# My Custom Oh My Posh Theme Setup

This guide will help you set up the **My-Custom-Theme-OMP** for Oh My Posh on a new PC. Follow the steps below to get started.

## Prerequisites

Before proceeding, ensure that the following tools are installed on your PC:

- **Windows Terminal** or another terminal emulator (like PowerShell or Git Bash)
- **Oh My Posh**
- **Font with Nerd Fonts** (for icons and symbols)

---

## Step 1: Install Oh My Posh

1. **Windows Installation**:
   - Open PowerShell as Administrator and run:

     ```bash
     winget install JanDeDobbeleer.OhMyPosh
     ```

   - Confirm that Oh My Posh is installed by running:

     ```bash
     oh-my-posh --version
     ```

2. **Linux/macOS Installation**:
   - You can install via Homebrew:

     ```bash
     brew install jandedobbeleer/oh-my-posh/oh-my-posh
     ```

   - Or via package manager for your distribution.

---

## Step 2: Install a Nerd Font

Your custom theme uses icons and symbols from Nerd Fonts. Follow these steps to install a Nerd Font:

1. Download a Nerd Font from [Nerd Fonts GitHub](https://github.com/ryanoasis/nerd-fonts/releases).
2. Install the font on your PC.
3. Configure your terminal to use the installed Nerd Font.

   - For Windows Terminal:
     - Open `Settings > Profiles > Appearance`.
     - Change the font face to the Nerd Font you installed.

---

## Step 3: Clone the Custom Theme Repository

Clone the repository containing your custom Oh My Posh theme:

```bash
git clone https://github.com/hmsmiraz/My-Custom-Theme-OMP.git
```

---

## Step 4: Apply the Custom Theme

1. Open the terminal where you want to apply the theme.
2. Navigate to the folder where you cloned the repository:

   ```bash
   cd My-Custom-Theme-OMP
   ```

3. Copy the theme JSON file to the Oh My Posh themes directory:

   ```bash
   cp ./my-custom-theme.json ~/.poshthemes/
   ```

   (For Windows, you might want to copy it to `C:\Users\<YourUsername>\AppData\Local\Programs\oh-my-posh\themes`).

---

## Step 5: Configure Oh My Posh to Use the Custom Theme

1. Open your terminal's configuration file:
   - **For PowerShell**: Edit your `$PROFILE`:

     ```bash
     notepad $PROFILE
     ```

   - **For Git Bash or other terminals**: Open `.bashrc` or `.zshrc` in your home directory.

2. Add the following line to set the custom theme:

   ```bash
   oh-my-posh init pwsh --config ~/.poshthemes/my-custom-theme.json | Invoke-Expression
   ```

   (For other terminals, change `pwsh` to `bash` or `zsh` as needed).

3. Save and close the file.

---

## Step 6: Reload the Terminal

After updating the configuration file, reload your terminal:

- For PowerShell: Run `& $PROFILE`
- For Bash/Zsh: Run `source ~/.bashrc` or `source ~/.zshrc`

Your terminal should now display the custom Oh My Posh theme!

---

## Step 7: Customize as Needed

You can further customize your theme by editing the `my-custom-theme.json` file.

---

## Troubleshooting

- **Icons Not Displaying Correctly**: Ensure that you are using a Nerd Font in your terminal settings.
- **Theme Not Applied**: Check if the path to the theme file is correct in your configuration file.

---

That's it! You now have your custom Oh My Posh theme up and running on your new PC.
```
