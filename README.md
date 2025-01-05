# SnigdhaOS SDDM Configuration 🎨✨

This repository contains configuration files and resources for customizing the **Simple Desktop Display Manager (SDDM)** used in **SnigdhaOS**. SDDM is a modern, lightweight display manager for X11 and Wayland that allows users to log into their desktop environment.



## Table of Contents 📑

1. [Overview](#overview)
2. [Features](#features)
3. [Directory Structure](#directory-structure)
4. [Installation](#installation)
5. [Customization](#customization)
6. [Contributing](#contributing)
7. [License](#license)



## Overview 🖥️

The **SnigdhaOS SDDM Configuration** repository provides a preconfigured theme and settings tailored for SnigdhaOS. The goal is to offer a visually appealing and seamless user experience for SnigdhaOS users when logging into their system.

### Key Highlights:
- 🎨 A custom SDDM theme designed for SnigdhaOS.
- ⚙️ Predefined settings for optimal performance and aesthetics.
- 🖱️ Compatibility with various desktop environments.



## Features 🌟

- **Custom Theme**: A SnigdhaOS-branded SDDM theme with unique colors, logos, and styles.
- **User-Friendly**: Preconfigured options to make setup straightforward.
- **Lightweight and Modern**: Ensures a fast and smooth login experience.
- **Wayland and X11 Support**: Works seamlessly across both graphical display protocols.



## Directory Structure 📂

```
.
├── themes/                # Custom SDDM themes
│   └── snigdhaos/         # Main theme directory
│       ├── theme.conf     # Theme-specific configuration
│       ├── background.png # Background image for the login screen
│       ├── icons/         # Custom icons for the theme
│       └── ...            # Other theme-related assets
├── sddm.conf              # Main SDDM configuration file
├── LICENSE                # License information
└── README.md              # Project documentation
```



## Installation 🛠️

Follow these steps to set up the SnigdhaOS SDDM configuration on your system:

### Prerequisites 📋
- Ensure SDDM is installed on your system. For most Linux distributions, you can install it using the package manager:

  ```bash
  # For Debian/Ubuntu-based systems:
  sudo apt install sddm

  # For Fedora-based systems:
  sudo dnf install sddm

  # For Arch-based systems:
  sudo pacman -S sddm
  ```

- Clone this repository:

  ```bash
  git clone https://github.com/Snigdha-OS/snigdhaos-sddm-config.git
  cd snigdhaos-sddm-config
  ```

### Setup Steps ⚙️

1. **Copy the Theme**:
   Copy the custom theme to the SDDM themes directory:

   ```bash
   sudo cp -r themes/snigdhaos /usr/share/sddm/themes/
   ```

2. **Apply the Configuration**:
   Replace the default SDDM configuration with the one provided:

   ```bash
   sudo cp sddm.conf /etc/sddm.conf
   ```

3. **Enable SDDM** (if not already enabled):

   ```bash
   sudo systemctl enable sddm
   sudo systemctl start sddm
   ```

4. **Set the Theme**:
   Edit the SDDM configuration file to use the SnigdhaOS theme:

   ```bash
   sudo nano /etc/sddm.conf
   ```

   Update the `[Theme]` section as follows:

   ```
   [Theme]
   Current=snigdhaos
   ```

   Save and exit.

5. **Restart SDDM**:
   Restart the SDDM service to apply changes:

   ```bash
   sudo systemctl restart sddm
   ```



## Customization 🎨

You can further customize the SDDM theme and settings:

### Modifying the Theme
- **Background Image**: Replace the `background.png` file in the theme directory with your desired image.
- **Icons and Colors**: Edit the CSS or image assets in the `themes/snigdhaos/` directory to adjust the theme's appearance.

### Editing SDDM Configuration
- Open `/etc/sddm.conf` to modify various settings like autologin, session defaults, or display settings.
- For more details, refer to the [SDDM Configuration Manual](https://github.com/sddm/sddm/wiki/Configuration).



## Contributing 🤝

We welcome contributions to improve the SnigdhaOS SDDM configuration! To contribute:

1. Fork the repository.
2. Create a new branch for your changes:

   ```bash
   git checkout -b feature/your-feature-name
   ```

3. Make your changes and commit them:

   ```bash
   git commit -m "Add your commit message here"
   ```

4. Push your changes and open a pull request:

   ```bash
   git push origin feature/your-feature-name
   ```

Please ensure your changes are well-documented and tested.



## License 📜

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute this project as long as proper credit is given.



## Contact 📧

For any questions or support, please open an issue in this repository or contact the SnigdhaOS team at [support@snigdhaos.org](mailto:support@snigdhaos.org).



Thank you for using SnigdhaOS SDDM Configuration! We hope it enhances your SnigdhaOS experience. 🎉

