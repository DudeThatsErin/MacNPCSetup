# Erin's Mac & Windows PC Setup for Full Stack Development
You can `CTRL + F` to find your way through this guide. I have split it up between my Windows PC and my Mac.

> ***NOTE:*** None of the links included to apps or devices I use are affiliate links. I'm not looking to make money, just provide informative info to anyone who wants it.

## What Computers do I have?
### Windows PC
I have an older iBuyPower PC that I regret buying now. It has the following specs:
- i7 7th Gen
- NVIDIA Geforce 2080TI
- 12GB DDR4 RAM
- 750GB between 2 SSDs (250GB SSD has OS) (500GB SSD has extra files) + 2TB HDDs

My husband has a custom-built PC that I will be adopting when he upgrades. When I do those specs are as follows:
- i9 12th Gen
- NVIDIA Geforce 3080TI
- 64GB DDR5 RAM
- 3TB M.2 SSDs

### Mac
I got a 2023 MacBook Pro from work and the specs are as follows:
- Apple M3 Max Chip
- 16" Retina Display
- 36GB RAM
- 1TB M.2 SSD

### Peripherals
- [Logitech MX Craft Keyboard](https://www.logitech.com/en-us/products/keyboards/craft.920-008484.html)
  - I like it, but I recommend the [Logitech MX Keys S](https://www.logitech.com/en-us/products/keyboards/mx-keys-s.920-011559.html), the dial on the craft isn't that useful. I only got the craft to replace my MX Keys cause the battery doesn't last for very long though I switch back and forth between the keyboards all the time.
- [Logitech Master 3](https://www.amazon.com/Logitech-Master-Advanced-Wireless-Mouse/dp/B07XC2FWD1) which I recommend over the 3S as they are virtually the same thing and you can get this one for cheaper.
  - I got the 3S for work and I can confirm they are exactly the same. I don't notice ANY difference between the 2. Go with the MX Keys & Master 3 as they are cheaper and EXACTLY the same as the 3s and Keys S.
- 2TB M.2 SSD that I use as an external storage solution for both computers
- LG 55" 4K TV with an Apple TV Connected.
  - We have 2 of these TVs 1 model year apart. I believe they are 2021 and 2022. We have 2 Apple TVs. One is the latest model that just came in on July 1. 64GB 4k version. Our older one we got in 2021 and it is a 32GB 4K Apple TV.

## MacOS Setup
### Basic Apps
This is a quick list of the apps I use on my Mac.

- GitHub Desktop
- Safari
  - I don't like Arc because you can't open separate windows for things so using multiple monitors is a no-go with it. Chrome harvests too much data and uses too much RAM so I use Safari.
- Apple Mail / Spark
  - I haven't decided on which one I want to use so for now, I am using both.
- Apple Notes for Notes
- WP Engine Local to keep our sites up-to-date.
- Trello for work tasks and notes as well as personal projects. I use the free version as there is nothing in premium that is necessary for me since I don't share.
- AirTable for tasks that are shared at work. My employer uses AirTable to keep everything up-to-date.
- Harvest to keep track of time spent on work projects for billing purposes.
- Raycast as this is my spotlight app of choice.
- Freeform for notes while I'm learning math.
- Apple Reminders for tasks in my personal life.
- Apple Calendar to keep track of meetings for work.
- Warp for a terminal replacement.
- Discord for Social Media.
- VSCode for coding.

### Homebrew / Terminal / Shell
#### Homebrew
[Homebrew](https://brew.sh) allows us to install tools and apps from the command line or via Raycast (my usual install method).

To install it open the built-in Terminal app and run this command:

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

This will also install the xcode build tools which is needed by many other developer tools.

After Homebrew is done installing, we will use it to install Raycast and a few other things, which will then be used to install everything else we need.

#### Terminal
The first app I install is to replace the built in Terminal app.

I prefer [Warp](https://www.warp.dev/) because:
- You can write with an IDE-style editor
- You can arrow up on your keyboard and see your past commands you have done in the terminal.
- You can save commands to reuse later.
- You can customize keybindings and launch configs.
- It has more preloaded custom themes or you can design your own.
- It also includes "Warp AI" to explain or debug errors. I don't use the AI but I can see how useful
- Clickable links inside the editor.
- Native OS Notifications

We install this using a Homebrew "cask". Casks are full applications, similar to what you would install from the Mac App Store.

```shell
brew install --cask warp
```

Once installed, launch it and customized the settings/preferences to your liking. These are my preferred settings. Easiest way to pull up the settings is to press `CMD + ,` that brings up the settings in *every* app.

- Appearance 
  - Themes
    - Sync with OS: Enabled
    - Window Opacity: 100%
    - Blur Radius: 1
    - Input position: pin to the bottom (warp default)
    - Current Prompt: Warp Prompt (default)
    - Dim inactive panes: Disabled
    - Compact Mode Blocks: Disabled
    - Show Jumpt ot he bottom of block button: Enabled
    - Terminal Font: JetBrains Mono
    - Font Size 13
    - Line Height 1.2
    - Blinking cursor: Enabled
    - Show tab indicators: Enabled
  - Features
    - General
      - Shortcut screen on new tab: Enabled
      - Copy on Select: Enabled
      - Restore windows, tabs and panes on startup: enabled
      - Show sticky command header: Enabled
      - Show tooltip on click on links: Enabled
      - Choose an editor to open file links: WebStorm
      - Open Markdown files in Warps Markdown Viewer by Default: Enabled
      - Show warning before quitting: Disabled
      - Show warning before logging out: Disabled
      - Show changelong after updates: Disabled
    - Session
      - Warp SSH Wrapper: Disabled
      - Receive desktop notifications from Warp: Enabled
        - If a command takes longer than 30 seconds to complete: Enabled
        - If a command prompts you to enter a password: Enabled
        - Startup shell for new sessions: `bash (/bin/bash)`
        - Working directory for new sessions: home directory
        - Enable reopening of closed sessions: Enabled
          - Grace period (seconds): `60`
      - Keys
        - Left Option key is Meta: Disabled
        - Right Option Key is Meta: Disabled
        - Global hotkey: Disabled
      - Editor
        - Autocomplete quotes, parantheses, and brackets: Enabled
        - Trigger Command Inspector on hover: Enabled
        - Error underlining for commands: Enabled
        - Syntax highlighting for commands: Enabled
        - Open completions menu as you type: Disabled
        - Suggest corrected commands: Enabled
        - Expand aliases as you type: Enabled
        - Edit commands with Vim keybindings: Disabled
        - Show input hint text: Enabled
        - Tab key behavior: Open completions menu
      - Terminal
        - Enable mouse reporting: Enabled
        - Enable Scroll Reporting: Enabled
        - Enable Focus Reporting: Enabled
        - Use Audible Bell: Disabled
        - Double-click smart selection: Enabled
      - Workflows
        - Show global workflows in command search (`CTRL + R`): Disabled



### Git Setup
Open a new tab/window to start using the latest version:
```shell
git --version
```

Configure git with your name/email and preferred editor:
```shell
git config --global user.name dudethatserin

git config --global user.email erin@null.computer

git config --global core.editor nano
```

### NPM/Node/NVM Setup
I use node/npm to maintain my github repos and to install items while I am working. NVM is used to keep Node up to date.

### PHP Setup
I use PHP in my day job (which the Mac is for) and I use it for yarn and to install roots/sage and build our projects. I use PHP 8.3 which is the current latest version. We run these websites via WP Engine's Local desktop app.

# Windows PC Setup
When I am first setting up my Windows PC I set it up with the least amount of reporting back to Microsoft as possible. I do login to my Microsoft/Outlook account.

## Apps I install/use once setup
- Browser
  - I attempted to use [Arc](https://appseeker.org/dudethatserin/Arc-9ccf1de38481400e9aeab18fc33d3ebc?pvs=25) but I couldn't get logged in/registered and their discord server was no help. They never contacted me back via support either. So, while I use Arc on my Mac... On Windows, I use [Google Chrome](https://appseeker.org/dudethatserin/Chrome-805361ee66f64cb9a1208bbaafc4b2b7?pvs=25) since it is easy to install and it doesn't chew up RAM as much as [Microsoft Edge](https://appseeker.org/dudethatserin/Edge-2bef5ebf82974be9b562fd3472a7e6e5?pvs=25) did on my PC.
- Shell
  - Powershell
- Misc
  - Steam to play Palworld & Age of Empires IV.
  - ShareX for screenshots
  - Spark for Email

I don't do much customization on my Windows PC.

# Productivity & Other Apps

## Window Management - MacOS
On Windows I use the built-in app switch so this is focusing on Mac.

####  Raycast
This is an app I go over a lot more later but Raycast also has built-in window management.

```shell
brew install raycast
```

## App Switching - MacOS
On Windows I use the built-in app switch so this is focusing on Mac.

I use an app switcher that is **free** called [AltTab](https://alt-tab-macos.netlify.app). It shows the full window previews just like how Windows show them when you `CMD + TAB`.

I replace the `CMD + TAB` shortcut with AltTab
```shell
brew install alt-tab
```

## Screenshots
For both Windows and Mac I use custom screenshotting tools as the built-in options do not offer as many features. You can use them if you want but these options give you more features.

### MacOS
I use the built-in screenshotting tool. I used to use [Clean Shot X](https://cleanshot.com/) but I couldn't justify the cost (even for the $30 lifetime) when the built-in options for Mac are good enough.

### Windows
I use [ShareX](https://getsharex.com) to take screenshots. It also works just like the iOS Screenshot tool. I prefer the way the iOS Screenshot tool works (if you can't tell) as you don't have to download screenshots that you don't need for longer than 2 seconds that just take up needless space on your storage.

The **only** reason why I don't use the built-in tool is because ShareX is free. It doesn't do much that I can't do with the Clipping Tool.

## Task Management
I alternate between [Todoist](https://todoist.com), Apple Reminders, and [Things 3](https://culteredcode.com). Things 3 is a great app but it has shortcomings. I talk about them on my website, [App Seeker](https://appseeker.org). You can go through to App Seeker to read about each of them.

## Quick Launching
This only applies to Mac because Windows already has a "Quick Launcher" with the search built into the start bar, though it isn't anywhere near as good as Spotlight on Apple devices. Though the built-in spotlight search is a bit slow and doesn't have as many features as the search I use to replace it.

There are 2 options you can use. [Alfred](https://www.alfredapp.com) and [Raycast](https://raycast.com). 

I use Raycast as it is free and has **tons** of extensions built-in that I use (for free) and just works and looks similar to Apple's Spotlight search.

```shell
brew install raycast
```

It will guide you through setting up Raycast so that it will replace your spotlight search.

### Raycast Extensions
If you type in `extenisons` into the search you can see all of your extenions and if you type in `store` you can install new extensions.

These are the extensions I have and use (that are not built into Raycast):

- Apple Notes -> Search & Create notes within Apple Notes.
- Apple Reminders -> Manage Apple Reminders: Create Reminders, see Reminders in your Menu Bar and more.
- Brew -> Search and install Homebrew formulae.
  - Make sure to go into settings and enable the "Remove all files associated with a cask" that way extra files don't get leftover when you uninstall apps/casks.
- Calculator -> I do calculations in Raycast most of the time.
- Clean Keyboard -> Disables the keyboard so you can clean it.
- Color Picker -> Pick and organize colors, everywhere on your Mac.
- Create Quick Event -> Allows me to use natural language to create a new event in my calendar.
- Google Search -> Allows me to do a Google Search in the menu bar.
- Pomodoro -> This is a way for me to have Pomo timers in my menu bar.
- Kill Process -> Allows me to kill processes that may be stuck on my computer.
- Remove Paywall -> Allows me to remove paywalls from links.
- Safari -> Allows me to see all of my tabs open in Safari as well as my Reading List and History.
- Tailwind CSS -> I use Tailwind CSS at work and this makes it easy to look up items.
- System Monitor -> Just what the name is.
- Speedtest
- Warp -> Allows me to see my warp tabs/windows.
- Timers - Allows me to set timers. I use this for the Pomodoro technique which I don't use often but I use it when my ADHD gets really bad.

### Other Apps
- [Discord](https://discord.com)
- [Spark](https://sparkmailapp.com/) -> I use the free version to easiliy sync my emails between devices. Works better than Outlook and just as good as [Newton Mail](https://newtonhq.com/) used to when they actually supported their app. I prefer Newton Mail for the read receipts but I can't justify paying $50/year for something that is barely supported. I mean just look at their "[Community](https://community.newtonhq.com/)". It is sad.
- [GIMP](https://gimp.org) -> This is a free alternative to photoshop. I don't use it often but when I need it, I have it.
- Visual Studio Code -> I use VSCodium as it is the same thing without Microsoft's tracking.
- [Visual Studio](https://visualstudio.microsoft.com) -> I use this for my backend programming.
- [VLC](https://videolan.org) -> I use VLC to watch videos instead of the built-in Quick Time or Windows Media Player.
- [7-Zip](https://7-zip.org) for Windows & [keka](https://keka.io/en) for Mac -> Both allow me to unzip 7-Zip files as well as RAR files and other types as well.
- Slack -> For work messaging
- Safari on Mac & Google Chrome on Windows.

You can install *most of* these either by searching them with the Brew Extension or by adding this list of files to a apps.txt on your desktop to install these with Brew on MacOS:

```shell
discord
gimp
vlc
readdle-spark
slack
raycast
git
alt-tab
```

Any apps not listed above cannot be installed with Brew and have to be downloaded from their websites.

Run the following command on Mac to install the items with brew if you stored them in an apps.txt file:

```shell
xargs brew install < apps.txt
```

Windows users can use Chocolatey to install a similar way, and then you are good to go. Though I use [Chris Titus' Windows Utility](https://github.com/ChrisTitusTech/winutil) to manage these kinds of programs. It is super easy to run and use.

You can run it in one of the following ways:
```shell
iwr -useb https://christitus.com/win | iex
```
OR
```shell
irm https://christitus.com/win | iex
```
Courtesy of the issue raised at: [#144](https://github.com/ChrisTitusTech/winutil/issues/144)

if for some reason this site is not reachable from your country please try running it directly from github
```shell
irm https://raw.githubusercontent.com/ChrisTitusTech/winutil/main/winutil.ps1 | iex
```

If these don't work, please check his repo as the commands probably got updated and I haven't had a chance to update them here yet.

# MacOS Menu Bar Customizations
## Calendar on Menu Bar
I use itsycal on my menu bar to get my calendar to show up there. 

```shell
brew install itsycal
```
Or use Raycast's Brew Extension to install it.

I have it just show the calendar icon and I keep the stock date and time showing in the top right.

# Node.js & NVM
I use nvm to manage the installed versions of Node.js on my machine. This allows me to easily switch between Node.js versions depending on the project I'm working in.

See installation instructions [here](https://github.com/nvm-sh/nvm#installing-and-updating).

OR run this command (make sure v0.39.1 is still the latest)
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

After installation you'll want to add the following to your .bash_profile / .zshrc etc.

```sh
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" ## This loads nvm
```

Now that nvm is installed, you can install a specific version of node.js and use it:

```sh
nvm install 18
nvm use 18
node --version
```

### Global Modules

There are a few global node modules I use a lot:

* lite-server
  * Auto refreshing static file server. Great for working on static apps with no build tools.
* license
  * Auto generate open source license files
* gitignore
  * Auto generate `.gitignore` files base on the current project type

```
npm install -g lite-server license gitignore
```
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

After installation you'll want to add the following to your .bash_profile / .zshrc etc.

```sh
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" ## This loads nvm
```

Now that nvm is installed, you can install a specific version of node.js and use it:

```sh
nvm install 18
nvm use 18
node --version
```

### Global Modules

There are a few global node modules I use a lot:

* lite-server
  * Auto refreshing static file server. Great for working on static apps with no build tools.
* license
  * Auto generate open source license files
* gitignore
  * Auto generate `.gitignore` files base on the current project type

```
npm install -g lite-server license gitignore
```
