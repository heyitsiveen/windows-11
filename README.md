# Windows 11 Fresh Install (VanTal)

This guide will walk you through setting up a fresh installation of Windows 11 for development, including updating the system, installing necessary tools, and configuring your environment.

### Set Up Windows 11

1. Update Windows 11 via **Windows Update**.
2. Update drivers using **Driver Booster**.
3. Restart your PC.
4. Repeat steps 1 and 2 to check for any remaining updates.
5. Uninstall unnecessary pre-installed apps.
6. Update your apps in the **Microsoft Store**.

### Set Up Development Tools

1. **Git**

   Install Git by running the following command:

   ```powershell
   winget install --id Git.Git -e --source winget
   ```

   Alternatively, you can download Git from their [official website](https://git-scm.com/downloads/win).

2. **Node.js (LTS version)**

   Install Node.js by following [Node.js Download](https://nodejs.org/en/download)

3. **JetBrainsMono Nerd Font**

   Install via [winget](https://winstall.app/apps/DEVCOM.JetBrainsMonoNerdFont)

4. **Windows Terminal**

   Configure Windows Terminal to your preferences.

5. **Oh My Posh**

   Install `Oh-My-Posh` by following [Oh-My-Posh Windows Installation](https://ohmyposh.dev/docs/installation/windows#installation)
   Copy or download my theme `heyitsiveen.omp.json`

   ```shell
   curl -o .config/oh-my-posh/heyitsiveen.omp.json https://raw.githubusercontent.com/vntbln/ubuntu/main/.config/oh-my-posh/heyitsiveen.omp.json
   ```

6. **Terminal Icons**

   Install `Terminal Icons` by following [Terminal-Icons Installation](https://github.com/devblackops/Terminal-Icons?tab=readme-ov-file#installation)

7. **Zoxide**

   Install `Zoxide` for smarter directory navigation by following [Zoxide Installation](https://github.com/ajeetdsouza/zoxide?tab=readme-ov-file#installation)

8. **Eza**

   Install `Eza` a modern replacement for `ls` by following [Eza Installation](https://github.com/eza-community/eza?tab=readme-ov-file#installation)

9. **FZF**

   Install `FZF` for fuzzy searching by following [FZF Windows Packages](https://github.com/junegunn/fzf?tab=readme-ov-file#windows-packages)

10. **PSFZF**

    Install `PSFZF` for integrating `FZF` with PowerShell by following [PSFZF Installation](https://github.com/kelleyma49/PSFzf?tab=readme-ov-file#installation)

11. **Set PowerShell Configuration Path**

    Set your default PowerShell profile configuration by editing `$PROFILE`:

    ```powershell
    New-Item -Path $PROFILE -ItemType File -Force
    notepad $PROFILE
    ```

    Add the following line to the file:

    ```powershell
    . $env:USERPROFILE\.config\powershell\user_profile.ps1
    ```

12. **Copy Configuration Files**

    Copy all configuration files from the `.config` folder to your local system.

13. **Cursor AI Editor**

    Install `Cursor AI Editor` by following [Cursor AI Editor Download](https://www.cursor.com/)

14. **Bun & PNPM**

    Install `Bun` by following [Bun Windows Installation]([https://bun.sh/)](https://bun.sh/docs/installation#windows)
    Install `PNPM` by following [PNPM Windows Installation](https://pnpm.io/installation#on-windows)

15. **Wezterm (Optional)**

    Install `Wezterm` by following [Wezterm Installation](https://wezfurlong.org/wezterm/installation.html)

    Create Wezterm Config File

    ```shell
    mkdir -p ~/.config/wezterm
    nano ~/.config/wezterm/wezterm.lua
    ```

    or

    ```shell
    curl -o .config/wezterm/wezterm.lua https://raw.githubusercontent.com/vntbln/ubuntu/main/.config/wezterm/wezterm.lua
    ```

    Copy my wezterm.lua

    Exit and Re-run Wezterm
