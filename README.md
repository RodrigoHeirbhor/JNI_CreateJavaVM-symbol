Hi everyone and welcome! if you are a Tizen Studio user in Windows SO and would like to use it on MacOS as well to have a backup in case your Windows has a problem, here is a 14-step tutorial on how to fix a Tizen Studio bug that is happening in some previous versions of MacOS.

Screenshot (Copy and paste the link in a new tab):
[https://drive.google.com/file/d/1NoyTS6KKU9IQyHwVaT2TeT8euikdIfhz/view?usp=sharing](url)

Link to the bug discussion on the official Samsung Developers forum> https://forum.developer.samsung.com/t/tizen-studio-problem-on-macos-big-sur/9410?page=2

 This error appeared on my MacOS Monterrey 12.7.5 using the latest version of Tizen Studio 5.6 and I will leave the steps (How I solved it) below for anyone who faces this in the future:

🐛 (The JVM shared library “/users/username/Documents/Tizen Studio/jdk/Contents/Home/bin/…/jre/lib/server/libjvm.dylib” does not contain the
JNI_CreateJavaVM symbol.) 🐛

1- Download the latest version of Tizen Studio from the official link https://docs.tizen.org/application/vscode-ext/web/#develop-applications
2. Launch the Tizen Studio installer > When asked to define the workspace destination folder, create a new folder in Documents by clicking on the three dots in the installer and install in this new folder
3. Complete the entire installation and close the installer
4. Download VSCode from the official link to your Mac:
https://code.visualstudio.com/download
5. Install VSCode and download two more items: Python 2.7 and Node.js:
Python 2.7 Link for MacOS: https://www.python.org/ftp/python/2.7.18/python-2.7.18-macosx10.9.pkg
Node.JS Link for MacOS: https://nodejs.org/en/download/package-manager
6. To install Node.JS, just copy and paste this command into the VSCode terminal and press Enter/Return on MacOS:

# install nvm (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | party
# download and install Node.js (you may need to restart the terminal)
nvm 20 installation
# checks if the correct version of Node.js is in the environment
node -v # should print `v20.15.1`
# checks if the correct version of NPM is in the environment
npm -v # should print `10.7.0`

7. Open VSCode and download the "Tizen Web" extension, which is 3 extensions in 1

8. Open VScode Settings (Gear icon) > Command Palette > Type Tizen Web: Change the Tizen SDK path and press Enter.

9. In the notification that appears, copy the path that will be displayed and save it in a notepad > then click on 'Keep' to keep the current path, you don't need to change anything, the idea here is to just copy the path.
In this official link, there are more instructions on how to change the path: https://docs.tizen.org/application/vscode-ext/web/#develop-applications
10. Install the Tizen Baseline SDK by going to VScode settings (VScode gear icon), opening the command palette, and type "Tizen Web: Install the Tizen Baseline SDK"

11. In the notification that appears, do one of the following:

# If the SDK is already installed, click YES and run Tizen Web: Change SDK Path.

# If the SDK is not installed, to perform a new installation, click NO. In the notification that appears:

To start installing the Tizen Baseline SDK, click Install.
If the popup path is null, change the path by clicking Change Path and paste the path you saved in step 9.

12. Change the workspace path by going to VSCode settings (gear icon) and typing in the command palette: Tizen Web: Change workspace path and press Enter
In the notification that will be displayed, click to change the path and paste the same path that you copied in step 9.

13. Open Tizen Studio using the icon that can be found in Launchpad > The error will no longer be displayed

14. Open the package manager and download the additional resources that you will use in your project, then open Tizen Studio and be happy!!!
