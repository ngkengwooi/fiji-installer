# fiji-installer
Inno Setup script to create Windows installers for [Fiji (Is Just ImageJ)](https://imagej.net/Fiji).

## Where's the installer?

I have not provided an installer as I am not sure whether the licence allows me to redistribute the software including the bundled JRE. Frankly I have no time to read through all the licences at the moment. So I am providing the script and instruction on how to create the installer instead. 

## How to create the installer

1. You will need [Inno Setup](https://jrsoftware.org/isdl.php). Download the Unicode Inno Setup self-installing package and install it on your Windows computer.
2. Open the appropriate `.iss` script from this repository in Inno Setup:
  - `fiji-win32.iss` is for the 32-bit version of Fiji
  - `fiji-win64.iss` is for the 64-bit version of Fiji
3. Download the appropriate (32- or 64-bit) Fiji binary package from [the official site](https://imagej.net/Fiji):
  - For 32-bit Windows: https://downloads.imagej.net/fiji/latest/fiji-win32.zip
  - For 64-bit Windows: https://downloads.imagej.net/fiji/latest/fiji-win64.zip
4. Extract the ZIP archive so that the `Fiji.app` folder is in the same folder as the `.iss` file.
5. Adjust the version number (`#MyAppVersion`) in the `.iss` file, as appropriate.
  - I am not too sure what to use for the version number myself. Looks like it's versioned by timestamp. You can check previous releases [here](https://downloads.imagej.net/fiji/archive/).
6. Click the Compile button in Inno Setup. This will create an installer named `fiji-<version>-win32-setup.exe` or `fiji-<version>-win64-setup.exe` in the same folder as the `.iss` file.
7. Run the installer to install Fiji on your Windows computer and verify that it works as intended.
