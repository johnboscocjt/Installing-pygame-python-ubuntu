# Installing-pygame-python-ubuntu
# Solving the fail to install pygame package for pyhton following in Debian/Ubuntu:
Check out the error below:

jbtechnix@jbtechnix:~$ pip install pygame
error: externally-managed-environment

× This environment is externally managed
╰─> To install Python packages system-wide, try apt install
    python3-xyz, where xyz is the package you are trying to
    install.
    
    If you wish to install a non-Debian-packaged Python package,
    create a virtual environment using python3 -m venv path/to/venv.
    Then use path/to/venv/bin/python and path/to/venv/bin/pip. Make
    sure you have python3-full installed.
    
    If you wish to install a non-Debian packaged Python application,
    it may be easiest to use pipx install xyz, which will manage a
    virtual environment for you. Make sure you have pipx installed.
    
    See /usr/share/doc/python3.12/README.venv for more information.

note: If you believe this is a mistake, please contact your Python installation or OS distribution provider. You can override this, at the risk of breaking your Python installation or OS, by passing --break-system-packages.
hint: See PEP 668 for the detailed specification.

# How to solve the error above
Solutions:
Use a Virtual Environment: This is the most common and recommended solution. You create a virtual environment where you can freely install packages without affecting the system-wide Python environment.

Steps:
1. First, make sure you have python3-venv installed on your system. You can install it via:
   ```bash
   sudo apt install python3-venv
   ```
2. Create a virtual environment:
    ```bash
   python3 -m venv myenv
   ```
4. Activate the virtual environment:
    ```bash
   source myenv/bin/activate
   ```
6. Now, install pygame:
    ```bash
   pip install pygame
   ```
8. When you're done, you can deactivate the virtual environment with:
    ```bash
   deactivate
   ```

# Another solution 1:
Use pipx: pipx is a tool to run Python applications in isolated environments. It is especially useful for installing and running Python applications that are not packaged as part of the system.
Steps:

1. First, make sure pipx is installed:
   ```bash
   sudo apt install pipx
   ```
3. Install pygame using pipx:
   ```bash
   pipx install pygame
   ```
This will install pygame in an isolated environment, ensuring that your system Python remains unaffected.

# Another solution 2:
Use --break-system-packages (Not Recommended): This option bypasses the system restrictions and forces pip to install the package globally. However, using this can potentially break your system's Python installation and package management. It’s generally not recommended unless you know what you’re doing.

To force the installation with this option:
```bash
sudo pip install pygame --break-system-packages
```

The best option is to either create a virtual environment or use pipx. Both will allow you to install and manage pygame independently from the system Python environment.

# johnboscocjt/jbtechnix

