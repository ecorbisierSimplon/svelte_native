# **App Mobil Android Ubuntu**

<a id="markdown-**app-mobil-android-ubuntu**" name="**app-mobil-android-ubuntu**"></a>

<!-- TOC -->

- [**App Mobil Android Ubuntu**](#app-mobil-android-ubuntu)
  - [INSTALLATION](#installation)
    - [**Install Android Studio from the app store**](#install-android-studio-from-the-app-store)
    - [**Install NodeJs and NPM :**](#install-nodejs-and-npm-)
      - [METHOD CLI](#method-cli)
      - [OTHER POSSIBILITY for nodejs and npm](#other-possibility-for-nodejs-and-npm)
    - [**Install JDK**](#install-jdk)
    - [Environnement Variable](#environnement-variable)
    - [NativeScript](#nativescript)
    - [RUN](#run)
      - [in local with Android](#in-local-with-android)
      - [in Nativescript](#in-nativescript)

<!-- /TOC -->
<!-- /TOC -->

## INSTALLATION

<a id="markdown-installation" name="installation"></a>

[used docs.nativescript.org](https://docs.nativescript.org/setup/linux)
Use latest version for installation !!!

### **Install Android Studio from the app store**

<a id="markdown-**install-android-studio-from-the-app-store**" name="**install-android-studio-from-the-app-store**"></a>

- [Android Studio , trois façons de l'installer sur Ubuntu](https://ubunlog.com/fr/android-studio-instalacion-ubuntu/)

### **Install NodeJs and NPM :**

<a id="markdown-**install-nodejs-and-npm-%3A**" name="**install-nodejs-and-npm-%3A**"></a>

#### METHOD CLI

<a id="markdown-method-cli" name="method-cli"></a>

- Install NodeJs if not installed
  - Test with vesrion :
  - latest version in 02-07-2024 is v20.11.0

```cli=
node -v
```

if not installed :

```cli=
# On Ubuntu 22.04, we used the following command to install latest node
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -

sudo apt-get install -y nodejs

```

- Install npm if not installed
  - Test with version
  - latest version in 02-07-2024 is v12.09

```cli=
npm -v
```

if not installed :

```cli=
sudo apt install npm
```

#### OTHER POSSIBILITY for nodejs and npm

<a id="markdown-other-possibility-for-nodejs-and-npm" name="other-possibility-for-nodejs-and-npm"></a>

[Download the Node.js source code or a pre-built installer for your platform (includes npm)](https://nodejs.org/en/download)

### **Install JDK**

<a id="markdown-**install-jdk**" name="**install-jdk**"></a>

```nginx=
sudo apt-get install -y openjdk-21-jdk
```

- To confirm JDK is installed correctly, run:

```powershell=
java --version
javac --version
```

### Environnement Variable

<a id="markdown-environnement-variable" name="environnement-variable"></a>

Configure the ANDROID_HOME environment variable for NativeScript to be able to find the Android SDK, and add the required tools to path.

Add the following lines to your shell profile, usually ~/.bash_profile or ~/.bashrc, or if you are using zsh then ~/.zshrc config file:

```powershell=
export ANDROID_HOME=$HOME/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

### NativeScript

<a id="markdown-nativescript" name="nativescript"></a>

Install the NativeScript CLI globally:

```powershell=
npm install -g nativescript
```

Verifying the environment​
To verify that the installation was successful, open a new Command Prompt window (to ensure the new environment variables are loaded) and run

```powershell=
ns doctor
```

```powershell=
# or for android only :
ns doctor android
```

```powershell=
# or for ios only :
ns doctor ios
```

***Sometimes you need to install typescript in global :***

```nginx
npm install -g typescript
```

### RUN

<a id="markdown-run" name="run"></a>

#### in local with Android

<a id="markdown-in-local-with-android" name="in-local-with-android"></a>

```powershell
ns run android
```

#### in Nativescript

<a id="markdown-in-nativescript" name="in-nativescript"></a>

```powershell
ns preview
```

```powershell
# This is possibility for android 
ns preview android
```

```powershell
# This is possibility for ios
ns preview ios
```
