# flutter_nix_config
A flake for Flutter project — but you'll need to download the SDK separately and have it available on your system.






---


# Flutter + Android + Nix Flake Template

This is a Nix Flake setup for Flutter development with Android support.  
It is designed to simplify your development environment while giving you more control over SDK versions and system dependencies.

## 🚀 Features

- Minimal downloads: If you already have the Android SDK installed on your system, there's no need to download large files again.
- Version control: You can manage NDK and other component versions directly via Android Studio.
- `.envrc` support using [`direnv`](https://direnv.net/) for automatic environment loading.
- Works well with VSCode and Android emulators (with a small manual step — see below).

---

## 🛠 Prerequisites

- [Nix](https://nixos.org/download.html) installe
- flake
- [`direnv`](https://direnv.net/) installed and enabled for your shell
- Android SDK installed manually on your system (e.g., via Android Studio)

---

## 📦 How to Use

1. **Create a new project using this template**:

   ```bash
   nix flake new my_flutter_app -t github:Amir-Hossein-Azimi/flutter_nix_config
   ```

2. **Navigate to your project folder**:
    
    ```bash
    cd my_flutter_app
    ```
    
3. **Build the development shell**:
    
    ```bash
    nix build .#devShells.x86_64-linux.default
    ```
    
4. **Enter the development environment**:
    
    ```bash
    nix develop .
    ```
    
5. **Allow the environment with direnv** (optional but recommended):
    
    ```bash
    direnv allow
    ```
    
    > Make sure you have `direnv` installed and enabled.  
    > If you're new to `nix-direnv`, check out this great article:  
    > [How to Learn Nix – nix-direnv](https://ianthehenry.com/posts/how-to-learn-nix/nix-direnv/)
    
6. **Open the project in VSCode or your preferred editor.**
   ```bash
   code .
   ```
    


---

## ⚠ Emulator Notes

To run the Android emulator, **you need to manually start it via Android Studio**.
Once it's running, VSCode will be able to detect it.

> If you know a better way to make the emulator work automatically with VSCode, feel free to open an issue or suggest improvements — contributions are always welcome!

---

## 💬 Feedback

If you find any improvements, fixes, or better configuration ideas, feel free to share! Pull requests and suggestions are very welcome.

---




