<h1 align="center">
  Javinizer (JAV Organizer)
  <br>
</h1>

<h4 align="center">A commandline or GUI based PowerShell module used to scrape metadata and sort your local Japanese Adult Video (JAV) files into media library compatible formats.</h4>

<br>

<p align="center">
  <a href="https://github.com/jvlflame/Javinizer/releases">
    <img src="https://img.shields.io/github/v/release/jvlflame/Javinizer?include_prereleases&style=flat&label=release"
         alt="GitHub">
  </a>
  <a href="https://www.powershellgallery.com/packages/Javinizer/y"><img src="https://img.shields.io/powershellgallery/dt/javinizer?color=red&label=psgallery%20downloads&style=flat"
  alt="PSGallery">
  </a>
  <a href="https://hub.docker.com/r/jvlflame/javinizer">
      <img src="https://img.shields.io/docker/pulls/jvlflame/javinizer?color=red"
      alt="Docker Hub">
  </a>
  <a href="https://discord.gg/Pds7xCpzpc">
    <img src="https://img.shields.io/discord/608449512352120834?color=brightgreen&style=flat&label=discord%20chat"
    alt="Discord">
  </a>
</p>

<p align="center">
  <a href="#key-features">Features</a> •
  <a href="#installation-&-usage">Installation</a> •
  <a href="https://docs.jvlflame.net/">Documentation</a>
</p>

<img src="https://github.com/jvlflame/Javinizer/blob/master/media/demo.gif" width="1280">
<img src="https://github.com/jvlflame/Javinizer/blob/master/media/demo-gui.jpg" width="1280">

-   [View GUI demo video here](https://gfycat.com/spiriteddefenselessgrouper)
-   [View GUI screens here](https://github.com/jvlflame/Javinizer/tree/master/media/gui)

## Features

**Highly customizable**. An array of scrapers are available for you to mix-and-match metadata with. Scrapers sources include sites such as Javlibrary, R18, Dmm (Fanza), JavBus, Jav321, AVEntertainment, MGStage, and DLGetchu. Various _.csv_ settings files are also provided to customize your metadata even further.

**Flexible file detection**. Multiple methods are provided to detect your local JAV files such as the built-in file matcher as well as a customizable regex string.

**Multi-language support**. Scraper sources provide Japanese, English, and occasionally Chinese language support. Machine translation modules are also available to translate individual metadata fields of your choosing.

**You manage your data**. Metadata _.nfo_ files are created for each JAV file to be read by a media library application. Contrary to a metadata plugin, if an online scraper suddenly disappears, you still keep your metadata.

## Installation

View the full Javinizer installation and usage documentation on [GitBook](https://docs.jvlflame.net/).

To run Javinizer, you will need to install following prerequisities:

-   [PowerShell 7](https://github.com/PowerShell/PowerShell)
-   [Python 3](https://www.python.org/downloads/)
    -   [Pillow](https://pypi.org/project/Pillow/)
    -   [googletrans >= 4.0.0rc1](https://pypi.org/project/googletrans/) or [google_trans_new](https://pypi.org/project/google-trans-new/)
-   [MediaInfo](https://mediaarea.net/en/MediaInfo/Download) (Optional)

**NOTE**: You will need to add Python to your system PATH. Windows calls `python`, while Unix/MacOS calls `python3`.

After installing the required prereuquisites, run the following command in an administrator PowerShell 7 console to install the Javinizer module:

```powershell
# Install the module from PowerShell gallery
C:\> Install-Module Javinizer

# Check that the module has been installed; if error, restart your console
C:\> Javinizer -v
```

### Quick start

Here are some common commands that you will be running with Javinizer:

```powershell
# Run a command to find metadata
C:\> Javinizer -Find "ABP-420" -Javlibrary

# Run a command to sort your JAV files using default settings
C:\> Javinizer -Path "C:\JAV\Unsorted" -DestinationPath "C:\JAV\Sorted"

# Open the Javinizer settings configuration
C:\> Javinizer -OpenSettings

# Update your Javinizer module
C:\> Javinizer -UpdateModule

# View the Javinizer commandline help (may not be fully up-to-date)
C:\> Javinizer -Help
```
