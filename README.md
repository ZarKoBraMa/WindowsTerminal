# WindowsTerminal

# Download:
- from Windows Store -> PowerShell
- from https://www.nerdfonts.com/ -> font: Jetbrains Mono Nerd Fonts
- from https://starship.rs/ -> go to terminal and type command: winget install --id Starship.Starship

# Open terminal:
- if error is shown related to execution policy, open terminal as admin and type: Set-ExecutionPolicy RemoteSigned
- Open Settings as JSON and in Schemas property as first in the list set next theme:
{
            "background": "#1A1A1A",
            "black": "#121212",
            "blue": "#2B4FFF",
            "brightBlack": "#666666",
            "brightBlue": "#5C78FF",
            "brightCyan": "#5AC8FF",
            "brightGreen": "#905AFF",
            "brightPurple": "#5EA2FF",
            "brightRed": "#BA5AFF",
            "brightWhite": "#FFFFFF",
            "brightYellow": "#685AFF",
            "cursorColor": "#FFFFFF",
            "cyan": "#28B9FF",
            "foreground": "#F1F1F1",
            "green": "#7129FF",
            "name": "zarkoba",
            "purple": "#2883FF",
            "red": "#A52AFF",
            "selectionBackground": "#FFFFFF",
            "white": "#F1F1F1",
            "yellow": "#3D2AFF"
        }

- In Settings of terminal (opened not as admin) set next:
  -- Default terminal application: Windows Terminal
  -- Default profile: PowerShell
  -- Save settings
  -- Click on Powershell profile and go to Appereance and set defult font: JetBrainsMono Nerd Fonts and in schemas choose zarkoba

- In terminal type:
  --Install-Module -Name Terminal-Icons -Repository PSGallery
  -- type $profile and PowerShell profile location will be dispayed. If this location or some of its part is missing create it.
  -- type code $profile and enter next content:
 $ENV:STARSHIP_CONFIG = "$HOME\.starship\starship.toml"
Invoke-Expression (&starship init powershell)
Import-Module -Name Terminal-Icons

# From this repo
- Download toml file
- In your machine create folde .starship under user profile folder and put toml file here
