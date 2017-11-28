Below are different setups I have on my machine that make me feel like I have the best dev box ever.  Generally, if there is a list, it is ordered by preference; most preferred to least preferred.  Feel free to make issues or ask me on [LinkedIn](https://www.linkedin.com/in/cwadrupldijjit?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base%3BmflX83jYQT%2Bg42wNPRW0BA%3D%3D), [Twitter](https://twitter.com/cwadrupldijjit), or [send me an email](mailto:sskeen9@gmail.com).  Best way to reach me though: Via Slack, if you know me (should be @cwadrupldijjit most places).

# Software

## General-Purpose

### Terminals
On Windows, there are basically two different command lines you can choose from: Cmd and Powershell.  Both are fairly simple to use and straightforward, though some may not care much for them (at the very least, my brother will never use Powershell if he can avoid it).  Many people use alternative terminals (particularly if they want a Bash experience over the default win32 architecture).  These are the terminals I use on my computer:

  1. [Hyper](https://hyper.is/) (which is also cross-platform, and built with Electron, with plugins available through npm and json configurations, and I believe is hackable)  
      - The default command line it uses is Cmd, but since I hate Cmd, I use **Powershell**.  I tried to set the default prompt to be powershell instead, but it didn't ever seem to work right, so I just type `powershell` each time I open a new window or tab.
      - I also mainly use this because it looks a whole lot nicer than the default terminals
      - This terminal has been buggy for me before, but lately, it's been on good behavior lately.
  1. Powershell
      - Powerful (and purportedly object-oriented) shell which takes what Cmd does and makes it much better, and allows you to use scripts called cmdlets (which may be available in Cmd?) to do what you want.  Some of the power of Powershell isn't really realized by me because I don't manage the system this way.  But the fact that most of the parameters and such are tabbable by default, this makes me like this much better than Bash
      - Despite my efforts in setting the defaults of the look of the windows, the fact that it has very limited customization options and the fact that the defaults were often ignored when loading the windows, I try to use this as little as possible, though will use this terminal over Cmd any day
      - I will have another section or document explaining how I've customized Powershell to look and feel its greatest
  1. Cmd
      - I don't enjoy using this terminal much, partially because it's much more limited than Powershell and makes me feel like I'm using an outdated machine
  1. Git Bash
      - Not worth the heartache and sorrow you will have when you use it.
      - I used to use this to ssh into other devices or at work so that I could use a thing called Vagrant.  After I installed a package to allow me to ssh from Powershell, I've blissfully forgotten this.

I've heard of a couple of other terminals that bounce around out there, but I've never found any reason to use them instead.  I'm pretty happy with Hyper + Powershell, so I'm keeping it.

### Editors
  1. [VS Code](https://code.visualstudio.com/) - hands-down winner
      - Usually use the Insiders builds (I'm too impatient to wait for new goodies!)
  1. [Visual Studio](https://www.visualstudio.com/)
      - For dabbling in other stuff, but usually collects dust
  1. [Android Studio](https://developer.android.com/studio/index.html)
      - Installed so I could maybe use the emulator for NativeScript development, but now is completely ignored, since Code does everything I need and it refuses to even open the emulator since I have Hyper-V enabled.
      - Included the ADB cli, which was really good, and now I don't need to use the IDE for it, anyway
  1. [PHPStorm](https://www.jetbrains.com/phpstorm/)
      - Used as little as possible--was installed because my work made me...
      - I also use the evaluation version so that I don't have to pay for something I won't likely use

Honorable mentions not currently installed on my computer (but still would rank above PHPStorm) are [Atom](https://ide.atom.io/) (since it's a solid editor, just not my favorite), [Brackets](http://brackets.io/), and even Vim (the in-terminal one, not the gui one you can get).

### Browsers
  1. [Chrome](https://www.google.com/chrome/browser/desktop/index.html)
      - Isn't perfect, is slightly slower than Firefox Quantum, but still has the most robust and easy-to use devtools out of the browsers I have on my computer
      - Also has all of the extensions I like to use
  1. [Firefox Quantum](https://www.mozilla.org/en-US/firefox/)
      - A beautiful update to the interface in my opinion.  Seems to be faster than Chrome.  I definitely think this is a step forward for it
      - I've had some problems with the devtools, though.  For instance, when I inspect the code, it seems like it suggests the same file twice.  I've also seen the devtools slowing down my computer/making the page with the tools open to it less responsive to my interaction, which has caused headaches while trying to develop, and effectively prevents me from using it for development.  Not a bad browser otherwise, though.
  1. [Edge](https://www.microsoft.com/en-us/windows/microsoft-edge)
      - Comes installed by default on Windows 10, and it is a much faster browser, and has better compatibility with ES2015+ than IE.
      - Webkit-based, so it should be able to do most of what you want with it
      - Not bad on browsing faster
      - Devtools not good enough for me
      - Has some weird CSS issues, but for the most part works fine
      - Also doesn't work with Vagrant and a virtual host setup so the setup for my job doesn't work with it (and from what I can tell, may not ever work with it).  Works fine for Node/localhost servers, just impossible to use with Vagrant
  1. [Internet ~~Exploder~~ Explorer](https://support.microsoft.com/en-us/help/17621/internet-explorer-downloads)
      - The old-and-not-too-reliable browser that will likely not ever work with modern web apps, and may very well be abandoned in future Windows versions
      - Barely deserves a mention, but will pick up virtual host configurations (unlike Edge), and allows to save self-signed-certificates so that you don't have to constantly make an exception in Chrome

### Social/Communication
  1. [Slack](https://slack.com)
      - Not completely bugless, but still a good collaboration tool
      - Has flexible functionality, and not bad for companies and communities
      - Uses markdown-like syntax for styling your messages
      - Has a sometimes useful but usually creepy Slackbot that lurks until it's unexpected
      - _Really_ annoying 10,000 message limit that means that you lose gems of knowledge over time
  1. [Discord](https://discordapp.com/)
      - Similar to Slack, but also includes voice channels, and is mainly geared toward gamers
      - Allows to do screen shares now
      - Supports more markdown-like syntax, but still isn't quite there
      - Has no message limits--what you say will be there forever unless you delete the message, or possibly the server itself is deleted
      - Doesn't support threads (which is a shame; Slack has spoiled me)
      - Isn't completely developer freindly, but works for the most part
  1. [HipChat](https://www.atlassian.com/software/hipchat)
      - Avoid this as much as possible
      - Work switched to HipChat from Slack, then realized our mistake, and switched back to Slack
      - Thankfully will be deprecated when the newer and much-more-anticipated [Stride](https://www.stride.com/) is released

## Windows configurations

### Developer Mode (Windows 10 only?)
You should be able to turn developer mode on in Settings > Update and Security > For developers > Use developer features > Developer mode (which may require you to push a button before you can select it).

### Hyper-V
Turned on if available.  Should be available for you if you are on a modern Windows Server or the Professional, Enterprise, or Education versions of Windows 8.1 or 10, and doesn't need to be installed.  It's a Windows feature, so you should be able to toggle it on by following [these instructions](https://blogs.technet.microsoft.com/canitpro/2014/03/10/step-by-step-enabling-hyper-v-for-use-on-windows-8-1/) (originally for 8.1, but should be similar for Windows 10).  If you're not sure if you can run Hyper-V, follow the instructions [in this article](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/reference/hyper-v-requirements#verify-hardware-compatibility).

### Bash on Windows
This is one of the coolest things ever.  This allows you to run bash from the command line.  Look for "Linux" in the Windows app store on Windows 10 Creators Update (should be the most current version), and there should be a banner that says roughly "Linux on Windows? Totally.", which you'd want to click the "Get the apps" button.  You can also just type in "Ubuntu", and it will pull up the Ubuntu "app" which allows you to run the Ubuntu bash from the command line.  There is an extra step you'd need to follow, but it explains that on the app details section.  With that, you can run in a full Ubuntu environment inside of Windows.

Now with this, you won't have the ability to use the same programs installed in Windows, since this is Linux and executables just aren't the same between those two environments.  As such, if you have Node installed outside of bash, you need to still install it for bash.  Same for npm or docker.

It's also possible that you could install Docker in bash because it's actually Ubuntu.  This is probably most useful if you are on a version of Windows that doesn't have Hyper-V, since Docker for Windows requires it, and Docker Toolbox doesn't require it but leaves a lot to be desired, and I've had struggles getting it to even half-work before.

## Web Development

### [Node](https://nodejs.org/)

Must-haves:
  - [`npm`](https://npmjs.org)
      - Did have some performance/undeterministic issues some people had which inspired someone else to try and do a better job, but since then has gotten over some of those issues and now is pretty darn fast and does (almost) everything that you'd need it to do
      - Get over it, Yarn!
  - [`windows-build-tools`](https://www.npmjs.com/package/windows-build-tools) - `npm i -g windows-build-tools`
      - Must be installed globally in an administrator console
      - This takes a while to install, so start it and then work on other things while you wait, and then check back on it every so often
      - Installs Python, Node-gyp, and also C/C++ compilers for building npm packages which need it
  - [`nvm-windows`](https://github.com/coreybutler/nvm-windows)
      - Solid Node Version Manager for windows (and apparently, eventually, posix) systems
      - Haven't used this to its full potential, but I am willing to use it if needs be
      - Probably will never use it to its full potential

Optional:
  - [`yarn`](https://yarnpkg.com/en/) - `npm i -g yarn`
      - May arguably be better than npm, but so far as I've seen, aside from some small conveniences, it isn't much better than npm

## Custom Configurations

### Powershell

#### Packages

Must-haves:
  - [Chocolatey](https://chocolatey.org/install)
      - Sorta like apt in Ubuntu or brew for macs, this allows you to customize your PC with a bunch of different packages you can use.
      - Used this to install the other packages listed
  - [`posh-git`](https://chocolatey.org/packages/poshgit/) - `choco install poshgit`
      - Awesome little command-line utility that gives you a small git summary in the command prompt, and also allows you to tab through branches (e.g. `git checkout mas<tab>` would fill out `master`), and has been beautiful for my work.
      - Further configuration I have is seen in the gist attached below for the Powershell profile files
  - [`openssh`](https://chocolatey.org/packages/openssh) - `choco install openssh`
      - Great package that allows you to use `ssh` commands from Powershell itself--no need to use Bash or Git Bash to do that.

Optional:
  - [`openssl`](https://chocolatey.org/packages/OpenSSL.Light) - `choco install openssl.light`
      - This allows you to generate SSL and TLS certificates to secure http and ws connections
      - Got this after realizing that the `node-greenlock` certificates were suspended from letsencrypt peeps due to the fact that they had those certificates publicly visible on GitHub, so I got the tool to allow me to generate my own certificates if needs be

#### Customizations
  - [Gist containing custom profile files](https://gist.github.com/cwadrupldijjit/db50b320c2b5a6c125367c51cc78c04e)

I generally have found that the tools built into powershell have been sufficient for my needs, but I got to a point where I needed to simplify some commands that I use all the time.  As such, you can see the `touch` function in one of the gists that I put together that would create files similar to how bash would do it.  I also put together a couple of functions that I could run to start/create a docker container with Postgres or Mongodb.  If people are interested, I could add that, too.

### Browser Extensions

Must-haves:
  - [Last Pass](https://www.lastpass.com/)
      - Browsers are good at storing passwords, but only for themselves.  LastPass extensions work in most browsers and has apps for phones and tablets.
      - You also can't manage them as well in browsers as LastPass can.
      - Also extremely useful if you need to share credentials, optionally without sharing the passwords themselves.
      - Can also be used to encrypt notes or important documents
  - [Wappalyzer](https://www.wappalyzer.com/)
      - Awesome little extension that usually can detect technologies/frameworks used on webpages
  - OneNote Clip Tool
      - Allows you to take screenshots, save images or PDFs, and more for webpages, and saves them into a new page in your OneNote app
      - Great if you use OneNote--similar extensions may be available for the note-taking apps of your choice
      - (more or less) Built into Edge
      - Extensions available for [Chrome](https://chrome.google.com/webstore/detail/onenote-web-clipper/gojbdfnpnhogfdgjbigejoaolejmgdhk?hl=en-US) and [Firefox](https://addons.mozilla.org/en-US/firefox/addon/onenote-clipper/)
  - [Honey](https://www.joinhoney.com/)
      - Finds and applies coupon codes for different websites
      - Integrates with some web pages to let you know if you're getting the best deal available on the site (such as with Amazon)

Optional:
  - [React DevTools](https://github.com/facebook/react-devtools)
      - Would only suggest it if you work with [React](https://github.com/facebook/react)
      - Allows you to inspect components, state, and props throughout the page; invaluable for your React app
  - [Augury](https://augury.angular.io/)
      - Would only suggest it if you work with [Angular](https://angular.io)
      - Allows you to inspect components, bound data, etc
      - Is only available in Chrome
  - [Adblock Plus](https://adblockplus.org/)
      - Guess why you'd want it ;)
      - Does a decent job blocking ads
      - Can also block some analytical software from tracking you
  - [Trello](https://chrome.google.com/webstore/detail/trello/dmdidbedhnbabookbkpkgomahnocimke?hl=en)
      - Create cards for Trello from your browser
      - Only official plugin is for Chrome
  - [WakaTime](https://wakatime.com/)
      - Tracks your time in projects, which is useful if you are a freelancer or need to track time spent on different projects
      - Also has extensions for [VS Code](https://wakatime.com/vs-code) and other [programs/IDEs](https://wakatime.com/#plugins)
  - [Rescue Time](https://www.rescuetime.com/)
      - Tracks your time in different activities, webpages, etc, which is useful if you are a freelancer or need to track time spent on different projects
      - Allows you to customize the category that the webpage/app you're using, and allows you to measure your productivity vs distractions
      - Also has desktop apps for tracking time spent per app

### VS Code Extensions

Must-haves:
  - [WakaTime](https://wakatime.com/vs-code)
      - Allows you to track your time spent per project, per language, etc., which can be interesting or good for freelancers
  - [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
      - Allows ESLint inline without having to run it separately
      - Requires ESLint to be installed globally (e.g. `npm i -g eslint`)
  - [TSLint](https://marketplace.visualstudio.com/items?itemName=eg2.tslint)
      - Allows TSLint inline without having to run it separately
      - Requires TSLint to be installed globally (e.g. `npm i -g tslint`)
  - [Quokka.js](https://marketplace.visualstudio.com/items?itemName=WallabyJs.quokka-vscode)
      - Allows you to run a "live scratchpad" for JavaScript or TypeScript inside VS Code
      - Requires Node to run, and usually requires a `console.log` statement in order to inspect data
  - [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
      - Allows you to type in a path to a file and helps you to know where you are
  - [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
      - Allows you to run selected code or a file in multiple different languages from Code
  - [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
      - Allows you to have better icons in the folder explorer on the left
  - [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)
      - An ingenious little extension which saves your current Code configuration to a GitHub gist so you can sync your settings across all of your devices which have VS Code installed
      - This includes but isn't limited to User Settings, Extensions, custom keyboard shortcuts, etc
      - Due to VS Code's nature, it's also cross-platform compatible, though you may need to put in keyboard shortcuts for both Mac and Linux/Windows if you work on both environments

Optional:
  - [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
      - Allows you to run a live server in the project root (automagically opens the current file in the browser after starting the server)
      - Only really useful for static sites--other websites might be better off using Webpack Dev Server or other similar tools
  - [Git Lens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
      - Allows you to see git blame annotations inline with the code and does a couple of other cool things Code can't do on its own
  - [SVG Preview](https://marketplace.visualstudio.com/items?itemName=kisstkondoros.svgpreview)
      - Allows you to see SVGs inside of VS Code if you want, just like JPGs, PNGs, etc.
      - Still will open the SVG file (code editor) unless you ask for a preview of it specifically
  - [SVG (Language support)](https://marketplace.visualstudio.com/items?itemName=jock.svg)
      - Makes working with SVGs a whole lot easier
  - [Angular Language Service](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template)
      - Superpowers your Angular 2+ app building, allowing you to have intellisense and other things in your templates along with much, much more
      - A must-have if you develop in Angular
  - Many, many extensions for different color schemes
      - Because the default ones are boring or can make you gag
