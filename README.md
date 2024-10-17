# Introduction to virtual environments

Python has a wide array of libraries with different versions and many dependencies that you can install on your computer to aid in your research. What do you do when you want to install a new library with dependencies that would conflict with another library you use? The answer is to define self-contained virtual environments. In this workshop, we will cover why and how to create virtual environments for your Python code development.

**Prerequisites:** Participants should be familiar with Python at the level of the Python Fundamentals Bootcamp, another introductory Python workshop, or be a self-taught Python coder.

## Installation

Prior to the workshop, please install either Anaconda or miniforge (not both) and ensure that you are able to access the installed Python.  Below are instructions on how to install either of these.  How do you choose which to install?

Install Anaconda if:
- You are new to Python
- You are not comfortable working from the command line, and prefer point and click applications
- You want an easy 1-click installation solution
- You are OK with slower load times and some level of "bloatware"
- You will not use this installation of Python for commercial purposes while at Northwestern

Install miniforge and related software if:
- You are an experienced coder
- You are willing to work (minimally) from the command line
- You don't want any bloatware
- You would prefer to use open-source software
- You may use this Python installation for commercial research

*If you are unsure which path to take, you should probably choose the first option and install Anaconda.*

### Option 1: Install the Anaconda Distribution

1. [Click here to go to the Anaconda download page.](https://www.anaconda.com/download)
2. Provide your email address,  agree to their terms, and download the installer.
3. Run the installer on your computer.
4. Open the Anaconda Navigator application on your computer (has a green circle icon).  
5. Within the Navigator, click on the Jupyter Notebook (or Jupyter Lab) icon.  
6. In the notebook that launches, create a code cell and type `1+1` and then `Shift + Enter` (or `Shift + Return`) to exectute that cell.  If it returns `2` without any errors, then you have successfully installed Anaconda's Python, and you are ready to attend the workshop.

### Option 2: Install miniforge (and possibly other software)
1. [Click here to go to the miniforge GitHub repo.](https://github.com/conda-forge/miniforge)  Download the installer for your operating system, and run the installer on your computer.  Accept all the defaults.
2. I recommend that you install VS Code as your IDE.  [Click here to go to the VS Code website.](https://code.visualstudio.com/) Download the installer, and run the installer on your computer.  Accept all the defaults.
3. If you are on Windows, I recommend that you also install Git Bash (or work in WSL).  [Click here to go to the Git Bash website.](https://gitforwindows.org/)  Download the installer, and run the installer on your computer.  Accept all the defaults.  (If you are working on a Mac or Linux, you already have Bash installed.)
4. Open VS Code, and set the default terminal by typing `Ctrl + Shift + p` then searching in the top bar for `Terminal: Select Default Profile`.  For Windows users, select Git Bash.  Otherwise, select your default bash terminal for your OS.
5. Initialize `conda` (and `mamba`) from the terminal as follows.  Type `Ctrl + ~` to open the terminal window at the bottom of VS Code.  In the terminal type:
    ```
    ./miniforge3/Scripts/mamba.exe init bash
    ```
    (If you chose a non-standard installation path for miniforge, you may need to modify the command above to point to the proper file.) This will edit your `.bash_profile` (or `.bashrc`) file to initialize `conda` and `mamba` when you open a terminal.   Close this terminal (e.g., type `exit`).  Then every new terminal you open will have access to `conda`, `mamba` and the related `python`.
6. Within your terminal, create your first python virtual environment by typing:
    ```
    mamba create --name test-env python=3.12
    ```
    (and confirming that you do want to install the packages.)
7. On the left panel of VS Code, click on the top icon for the `Explorer`.  Then click `Open Folder`.  This should bring up a finder window allowing you to select (or create) a folder for code development.  Select a folder.  This should show all the files and sub-directories from that folder within the left side bar of VS Code.  
8. Place your mouse within that left side bar to reveal the tools at the top that allow you to create new folders and files.  (Alternatively, you can right-click in that side panel to open a menu.) Create a new file named `test.ipynb`.  Then click on that new file to open it (if it doesn't open automatically) in the main window of VS Code.
9. Within the `test.ipynb` portion of the VS Code window, click on `Select Kernel` (in upper right).  This may cause VS Code to ask you to install the `Jupyter` and `Python` extensions; install those as requested.  (You would only need to install these extensions once.)  After those extensions are installed (and after clicking on `Select Kernel`), you should see the option at the top panel for `Python Environments`.  Click on that, and then select your `test-env`.
10.  Within your `test.ipynb` file, create a code cell and type `1+1` and then `Shift + Enter` (or `Shift + Return`) to exectute that cell.  If it returns `2` without any errors, then you have successfully installed Python and `conda`/`mamba`, and you are ready to attend the workshop.

## Getting Help

If you have any trouble with the installation steps above, please [use this link to submit a consultation request](https://app.smartsheet.com/b/form/2f2ec327e6164f83b588b7bbe2e2b56f).  Someone on our team will be happy to help you! 