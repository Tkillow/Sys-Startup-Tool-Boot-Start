# 🔧 DriverTool - Windows Driver Management Utility

[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows-blue.svg)](https://www.microsoft.com/windows)

## Overview

DriverTool is a comprehensive Windows desktop application designed to simplify driver development and management tasks. It provides an intuitive graphical interface for operations that traditionally require manual registry editing and command-line tools.

### Why DriverTool?

Traditional driver management requires:
- Manual registry modifications
- Complex command-line operations (`sc start`, `sc create`, etc.)
- Administrative privileges for service control
- Multiple steps for simple operations

DriverTool streamlines all these tasks into a user-friendly interface, saving time and reducing errors during driver development and testing.

---

## ✨ Features

- **Driver Registration**: Automatically register NT-mode drivers without manual registry editing
- **Service Management**: Start, stop, and unload drivers with a single click
- **Driver Information**: View detailed driver properties and status
- **Extension Support**: Advanced features for power users
- **Clean Interface**: Modern, intuitive GUI built with wxWidgets
- **Developer-Friendly**: Designed specifically for Windows driver developers

---

## 📸 Screenshots

### Main Interface
![Default Style](https://github.com/dybb8999/DriverTool/blob/master/Picture/Default.jpg)

### Extensions Panel 1
![Extensions 1](https://github.com/dybb8999/DriverTool/blob/master/Picture/ExtPage1.jpg)

### Extensions Panel 2
![Extensions 2](https://github.com/dybb8999/DriverTool/blob/master/Picture/ExtPage2.jpg)

---

## 🚀 Getting Started

### Prerequisites

- **Operating System**: Windows 7 or later
- **Privileges**: Administrator rights required for driver operations
- **Visual Studio**: 2013, 2015, or 2017 (for building from source)
- **wxWidgets**: Version 3.1.1 or compatible

### Quick Start (End Users)

1. Download the latest release from the [Releases](https://github.com/) page
2. Extract the executable file
3. Right-click and select "Run as Administrator"
4. Start managing your drivers!

---

## 🛠️ Building from Source

### Step 1: Install Development Tools

Download and install **Visual Studio 2015** (or VS 2013/2017 as alternatives).

### Step 2: Build wxWidgets

1. Download [wxWidgets 3.1.1](https://www.wxwidgets.org/downloads/)
2. Extract the archive
3. Open the appropriate solution file in Visual Studio:
   - For VS 2015: `build/msw/wx_vc14.sln`
   - For VS 2013: `build/msw/wx_vc12.sln`
   - For VS 2017: `build/msw/wx_vc15.sln`
4. Build both Debug and Release configurations for Win32 and x64 platforms

### Step 3: Configure Project

1. Clone this repository:
   ```bash
   git clone https://github.com/dybb8999/DriverTool.git
   cd DriverTool
   ```

2. Open the project in Visual Studio

3. Configure wxWidgets library paths:
   - Go to **Project Properties** → **VC++ Directories**
   - Add wxWidgets include directory to **Include Directories**
   - Add wxWidgets lib directory to **Library Directories**

### Step 4: Build

1. Select your desired configuration (Debug/Release)
2. Select your target platform (Win32/x64)
3. Build the solution (F7 or Build → Build Solution)

### Step 5: Run

Double-click the generated executable or run from Visual Studio (F5).

---

## 📖 Usage

### Loading a Driver

1. Click **Browse** to select your `.sys` driver file
2. Enter a service name for the driver
3. Click **Register** to add the driver to the system
4. Click **Start** to load the driver into memory

### Unloading a Driver

1. Select the running driver from the list
2. Click **Stop** to unload it from memory
3. Click **Unregister** to remove it from the system (optional)

### Advanced Features

Access the **Extensions** tabs for additional functionality:
- Driver signing information
- Memory analysis tools
- Service configuration options

---

## ⚠️ Important Notes

- **Administrator Rights**: Always run DriverTool with administrator privileges
- **Driver Signing**: On Windows 10/11, test signing must be enabled for unsigned drivers
- **System Stability**: Improper driver operations can cause system crashes - use with caution
- **Development Only**: This tool is intended for driver development and testing environments

### Enabling Test Signing (Windows 10/11)

```cmd
bcdedit /set testsigning on
```

Restart your system after enabling test signing.

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues, fork the repository, and create pull requests.

### Development Guidelines

1. Follow the existing code style
2. Test thoroughly before submitting pull requests
3. Update documentation for new features
4. Ensure compatibility with wxWidgets 3.1.1+

---

## 📄 License

This project is licensed under the Anti 996 License - see the [LICENSE](https://github.com/) file for details.

---

## 🔗 Resources

- [Windows Driver Development Documentation](https://docs.microsoft.com/windows-hardware/drivers/)
- [wxWidgets Documentation](https://docs.wxwidgets.org/)
- [Service Control Manager](https://docs.microsoft.com/windows/win32/services/service-control-manager)

---

## 💬 Support

If you encounter any issues or have questions:
- Open an [Issue](https://github.com)
- Check existing issues for solutions
- Consult Windows driver development forums

---

**⚡ Made for driver developers, by driver developers.**