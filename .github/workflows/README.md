# Living Notch Bongo Cat — Windows Desktop Application & Installer Package

## 1. End-User Installation Instructions (`LivingNotchBongoCat_Setup.exe`)
Once compiled via the included GitHub Actions Windows workflow or Inno Setup:
1. Double-click **`LivingNotchBongoCat_Setup.exe`**.
2. Choose your installation directory (defaults to `C:\Program Files\Living Notch Bongo Cat`).
3. Keep **"Launch Living Notch Bongo Cat automatically when Windows starts"** checked (and optionally check **"Create a desktop shortcut"**).
4. Click **Install** -> **Finish**. The application launches immediately at the top-center of your display without requiring Node.js, Rust, Python, or any terminal window.

## 2. Usage Guide
- **Auto-Hide Mini Bongo Cat Pod**: When idle or not hovered, the notch automatically collapses into a compact `78px × 38px` Mini Bongo Cat pod at the top-center of your screen framed by a circling neon border.
- **Hover to Expand**: Move your mouse cursor over the Bongo Cat pod to expand the full `480px × 205px` notch dashboard. Click **Pin** to keep it locked open.
- **YouTube & Spotify Sync**: Play any music on Spotify or in your browser (YouTube / YouTube Music). Windows SMTC automatically detects the song and fetches real-time synced `.lrc` lyrics from `LRCLIB`.
- **Charger Auto-Detection**: Plugging in your AC charger automatically transforms Bongo Cat from the Classic White mascot into the Neon Blue-Purple Gradient mascot and speeds up the circling neon border.
- **Always-on-Top Checklist & File Shelf**: Switch to the **Tasks** tab to manage your pinned to-do items, or drag-and-drop files onto the notch to store them in the **Shelf** tab.

## 3. Uninstallation Instructions
- Open **Windows Settings -> Apps -> Installed Apps** (or **Control Panel -> Programs and Features**).
- Locate **Living Notch Bongo Cat** and click **Uninstall**.
- The uninstaller automatically closes any running instance (`taskkill /F /IM LivingNotchBongoCat.exe`), removes all program files, and deletes the Windows Startup registry entry.

## 4. How to Compile the Binary Without Installing Dependencies on Your PC (GitHub Actions Cloud Build)
If you do not want to install Rust, Node.js, or Inno Setup on your local computer:
1. Upload this folder to a free GitHub repository.
2. GitHub's cloud `windows-latest` runner will automatically run `.github/workflows/build-windows-installer.yml`.
3. Go to the **Actions** tab on GitHub and download **`LivingNotchBongoCat-Windows-Release.zip`**, which contains the compiled **`LivingNotchBongoCat_Setup.exe`** and standalone **`LivingNotchBongoCat.exe`**.
