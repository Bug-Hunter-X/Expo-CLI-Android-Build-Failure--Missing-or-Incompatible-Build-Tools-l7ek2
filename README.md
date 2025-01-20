# Expo CLI Android Build Failure: Missing or Incompatible Build Tools

This repository demonstrates a common error encountered when building Android APKs using the Expo CLI.  The issue revolves around inconsistencies between the required Android SDK build tools version and what's installed on the system.  Even with a seemingly correctly configured Android SDK, the build process may fail.

The `expoBug.js` file illustrates a typical Expo project setup. The solution, in `expoBugSolution.js`, details how to address this incompatibility using the `expo prebuild` command with specific Android SDK build tools version configurations.

## Steps to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Attempt to build the Android APK using `expo prebuild`. Observe the error.
4. Apply the solution from `expoBugSolution.js` to resolve the error. 

## Solution

The solution involves using the `expo prebuild --android-sdk-build-tools-version=XYZ` command, substituting XYZ with a compatible version number of the Android SDK build tools.  The correct version may vary based on the Expo CLI version you are using; you may need to consult the Expo documentation for the most compatible version for your setup.  After running the prebuild command with the correct version the expo build:android command will build correctly