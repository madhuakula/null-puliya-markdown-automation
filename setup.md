# Setting up Markdown Automation


### Updating and Upgrading the system

- Run the below command to update and upgrade the operating system

```
$ sudo apt-get update && sudo apt-get upgrade
```

- Remove the old packages which are no longer required

```
$ sud apt autoremove
```

- Installing basic software properties by running below command

```
$ sudo apt-get install software-properties-common
```

### Installing `git`

- To install git in operating system, run the below command

```
$ sudo apt-get install git -y
```

### Installing web browser

- To install `chromium-browser` run the below command

```
$ sudo apt-get install chromium-browser
```

### Installing Sublime Text

- To install sublime text 3, navigate to the [Sublime Text website](https://www.sublimetext.com/)
- Click on download option and select the appropriate operating system to download.

- To download & install sublime text 3. Run the below commands

```
$ wget https://download.sublimetext.com/sublime-text_build-3126_amd64.deb
$ sudo dpkg -i sublime-text_build-3126_amd64.deb
$ rm sublime-text_build-3126_amd64.deb
```

#### Installing sublime text `Package Control`

- To install sublime plug-ins, first we have to install `package control`. Follow the below instructions to install package control
    + The instructions are taken from [https://packagecontrol.io/installation](https://packagecontrol.io/installation)
    + Open sublime text application, then access the console using  ``Ctrl +` `` (or) go to the `view -> show console`
    + Then paste the appropriate Python code for your version of Sublime Text into the console.

```
import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

- Then restart the sublime text application

#### Installing sublime text plug-ins

- Now we can install the plug-ins and start using package control
    + Once sublime text is opened, press `Ctrl + Shift + P` (or) go to the `Preferences -> Package Control` to install plug-ins
    + Now search for `install package` and press `enter` then type the package name you wanted to install.

**Some of the packages installed**

1. Markdown Preview
2. Markdown Editing
3. Git
4. Git Gutter
5. PlainTasks
6. SublimeCodeIntel
7. SideBarEnhancements
8. BracketHighlighter
9. Alignment

### Installing Terminator

- Terminator is a terminal software for Linux operating system, to install terminator run the below commands

```
$ sudo add-apt-repository ppa:gnome-terminator
$ sudo apt-get update
$ sudo apt-get install terminator
```

**Reference:** - [https://gnometerminator.blogspot.in/p/introduction.html](https://gnometerminator.blogspot.in/p/introduction.html)

#### Installing `hack` font and configuration

- To install `hack` font run the below command

```
$ sudo apt-get install fonts-hack-ttf
```

**Reference:** - [https://github.com/chrissimpkins/Hack](https://github.com/chrissimpkins/Hack)

- To configure this font in terminator, right click in terminator and navigate to the preferences and click on profiles tab.
- Uncheck the system fixed width font and select the `hack` font form the menu
- Then close the application

*Note:* Shout out to Akash for this (when I joined Appsecco, he told about this font and why to use this font)


### Installing Markdown Editor

- There are multiple editors available for markdown, for example Linux: [ReText](https://github.com/retext-project/retext), Mac: [MOU](http://25.io/mou/), Windows: [MarkdownPad](http://markdownpad.com)
- We are going to install `ReText`, to install run the below commands

```
$ sudo apt-get install retext
```

### Installing `Zeal`

- `Zeal` is an off-line documentation browser. Very useful! (MAC Alternative is - [Dash](https://kapeli.com/dash))
- To install zeal run the below commands

```
$ sudo apt-get install zeal
```

- To install documentations, open `zeal` application by menu (or) command `zeal` and follow the below instructions
    + Click on the `file` menu and click `zeal options`
    + Then navigate to the `Docsets` tab, in the downloadbale docsets check the documents you want and click `download`.
    + Once it completes download, you can see in the `installed docsets`

### Installing reveal-md

- [reveal-md](https://github.com/webpro/reveal-md) is a tool to convert markdown documents to [reveal.js](http://lab.hakim.se/reveal-js/) presentation format.
- To install `reveal-md` we need to have `npm` installed. First let's install `npm` by running the below command

```
$ sudo apt-get instlal npm
```

- For more information about installing nodejs can be found here [https://nodejs.org/en/download](https://nodejs.org/en/download/)

- To install `reveal-md` run the below command (*npm should be installed)

```
$ sudo npm install -g reveal-md
```

**Reference:** - [https://github.com/webpro/reveal-md](https://github.com/webpro/reveal-md)


### Installing Raneto

- [Raneto](https://github.com/gilbitron/Raneto) is a free, open, simple Markdown powered Knowledgebase for Node.js
- To install Raneto, follow the below commands

```
$ git clone https://github.com/gilbitron/Raneto.git
$ cd Raneto 
$ npm install
$ npm start
```

**Configuration**

- To configure `Raneto` edit the `example/config.default.js` for your requirements.

### Installing Gitbook

[Gitbook](https://github.com/GitbookIO/gitbook) is an easy to use solution to write, publish and host books. It is the easiest solution for publishing your content and collaborating on it.

- Run the below commands to install `Gitbook`

```
$ sudo npm install gitbook-cli -g
```

### Installing MkDocs

[MkDocs](http://www.mkdocs.org/) is a fast, simple and downright gorgeous static site generator that's geared towards building project documentation. Documentation source files are written in Markdown, and configured with a single YAML configuration file.

- To install `MkDocs` we need to have `python` and `pip` follow the below instructions
    + In most of the Linux operating systems `python` is installed by default. So I'm skipping installation of `python`

```
$ sudo apt-get install python-pip
$ sudo pip install --upgrade pip
$ pip install mkdocs
```

### Installing Pandoc

[Pandoc](http://pandoc.org/) is an universal document converter. If you need to convert files from one markup format into another, pandoc is your swiss-army knife.

- To install `Pandoc` follow the below instructions

```
$ wget https://github.com/jgm/pandoc/releases/download/1.19.1/pandoc-1.19.1-1-amd64.deb
$ sudo dpkg -i pandoc-1.19.1-1-amd64.deb
$ rm pandoc-1.19.1-1-amd64.deb
```

**Reference:** - [http://pandoc.org/installing.html](http://pandoc.org/installing.html)

### Installing `phantomjs`
- To install `phantomjs` run the below command

```
$ sudo apt-get install phantomjs
```

- It is used to take print of pdf from reveal-md


### Installing `GitBook Editor`
- To install GitBook Editor run the below command
```
$ wget http://downloads.editor.gitbook.com/download/linux-64-bit -O gitbookeditor.deb
$ sudo dpkg -i gitbookeditor.deb
$ rm gitbookeditor.deb
```

