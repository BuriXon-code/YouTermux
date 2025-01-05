# YouTermux

![screenshot](/youtermux.jpg)

## About ...

### What is YouTermux?

YouTermux is a bash and python script that is designed to download single or multiple videos/audios from YouTube without showing unnecessary ads, without monitoring your activity, without long conversion times, etc.

After receiving the appropriate input parameters, the script starts downloading the name/list of names of materials located on the YouTube platform at the provided URLs.

Then, after listing all the materials, the script starts downloading them (initially to .webm files) and then converting them to the selected format (audio/video).

Once the task is completed, the user receives an appropriate message and the script itself exits.

### What is the difference between youtermux and youlinux?

The youtermux script is a script dedicated to the Termux environment on mobile devices. The shebang, paths, and dependent packages in it have been adapted to those in the Termux environment.

The youlinux script is a version dedicated to the Linux x86 environment, which I wrote completely by the way. It works in essence identically, but because I don't do much work in the real GNU/Linux environment (mainly in Termux), the script may not work correctly (more on that at the bottom of the page in the "Compatibility" section).

### Is it legal?

Working with YouTube materials is not illegal. You can safely own the downloaded files for your own use.

Legality is violated when video/audio is shared in a manner inconsistent with prevailing regulations.

### Will it work forever?

Nope...

YouTube regularly updates the site's mechanisms and the API it provides, which can cause the script to stop working.

However, I will make an effort to keep the script working by analyzing changes made to YouTube and dependent packages.

### Why is it compiled?

The script was compiled by me as an experiment. I'm still learning, and compiling bash scripts was part of my learning.

I am not a hacker. I try to create utility scripts, simple tools and games. YouTermux script is not a backdoor, it does not make your device or system vulnerable to attacks.

If you'd like to see the source code, let me know (contact details at the bottom of the page).

![screenshot](/single.jpg)

## Installation and Usage ...

### Installation in Termux:

To install the package in Termux you need to initialize:

```
git clone https://github.com/BuriXon-code/YouTermux
cd YouTermux
chmod +x youtermux
```

>[!NOTE]
> Just in case, it is recommended to update the bash package first.

>[!TIP]
> Optionally, you can move the "youtermux" file to the "$PREFIX/bin" directory so that it can be run from the $PATH directory.

### Installation in Linux:

To install the package in any Linux distribution you need to initialize:

```
git clone https://github.com/BuriXon-code/YouTermux
cd YouTermux
chmod +x youlinux
```

The first time you run the script, it will notify you about the packages it needs and/or install them itself.

>[!WARNING]
> The script requires the "python" package to be installed, which is not present on some Linux distributions.
>
> To resolve, you need to install the "python-is-python3" package.

### Usage:

The script has a function that displays usage and parameter information along with simple usage examples and tips.

To view help and usage information, run:

```
./youtermux -h
```

or 

```
./youlinux -h
```

![screenshot](/help.jpg)

### Examples:

+ Downloading one video to the test.webm file:

```
./youlinux -v -o test -u https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

```
./youlinux --video --output test --url https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

+ Downloading one audio to the original name file:

```
./youlinux -a -u https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

```
./youlinux --audio --url https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

+ Downloading all video from a playlist to video01..video99 files:

```
./youlinux -v -o video -up https://www.youtube.com/playlist?list=PLE0hg-LdSfycrpTtMImPSqFLle4yYNzWD
```

```
./youlinux --video --output video --url-playlist https://www.youtube.com/playlist?list=PLE0hg-LdSfycrpTtMImPSqFLle4yYNzWD
```

+ Video download from all URLs in the file using Firefox cookies:

```
./youlinux -v -f <path-to-file> -c firefox
```

```
./youlinux -video -file <path-to-file> --cookies firefox
```

![screenshot](/playlist.jpg)

## Compatibility ...

### Enviroment:

### Errors:

### Dependencies:

### Version:

## Support ...

### Contact:

### Support me:
