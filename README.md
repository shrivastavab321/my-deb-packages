# 📦 My Debian Packages

This repository contains pre-built `.deb` packages for various tools and utilities I develop. These packages are built from separate, maintained source code repositories and are intended for easy installation on Debian-based systems like Ubuntu.

---

## 📂 Repository Structure

Each tool has its own folder with the following contents:

<tool-name>/
├── bin/ # Compiled binaries (no source code)
│ └── <tool>
├── debian/ # Debian packaging files (control, postinst, etc.)
├── build.sh # Script to generate .deb package
└── <tool>_<version>_all.deb

---

## ✅ Available Packages

| Tool        | Description                               | Version | Package |
|-------------|-------------------------------------------|---------|---------|
| `mytool`    | Remote-aware CLI for file operations      | 1.0     | [`mytool_1.0_all.deb`](./mytool/mytool_1.0_all.deb) |
| `setip`     | Static IP setter for Ubuntu (Netplan)     | 1.0     | [`setip_1.0_all.deb`](./setip/setip_1.0_all.deb)    |
<!-- Add more rows as you add tools -->

---

## 🚀 Installation Instructions

To install a `.deb` package manually:

```bash
wget https://github.com/<your-username>/my-deb-packages/raw/main/<tool>/<tool>_<version>_all.deb
sudo dpkg -i <tool>_<version>_all.deb

wget https://github.com/<your-username>/my-deb-packages/raw/main/mytool/mytool_1.0_all.deb
sudo dpkg -i mytool_1.0_all.deb

🛠️ How These Packages Are Built
Each tool is developed in a separate source code repository. The .deb files here are built using only the compiled binaries, not the source.
To build a package:

bash
cd <tool-name>
./build.sh
This uses dpkg-deb to package the compiled binary with its Debian control metadata.

📁 Source Code
🔐 The source code for each tool is maintained separately and may be private or public depending on the project. This repository contains only binaries and packaging metadata.

If you'd like access to the source or want to contribute, feel free to reach out.

📦 Future Plans
Add a GitHub Actions workflow to auto-build .deb files from source

Host a GitHub Pages-based APT repository

Add more Debian tools for networking, automation, and system utilities

📄 License
Each tool/package in this repository may have its own license. See individual folders for details. Packaging metadata is MIT licensed unless stated otherwise.

👋 Author
Badal Shrivastava
Maintainer of this Debian package archive.
GitHub • LinkedIn (optional)

🧰 More packages and updates coming soon!


