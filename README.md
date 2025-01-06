# YouTermux (beta) - YouTube Downloader

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

The "youtermux" script is written for the Termux environment. It was tested on 2 versions of Termux (0.118 and 0.119), on 2 CPU architectures (aarch64 and x86), on 4 devices, on 4 kernels. Each time it worked without major problems on aarch64 (mobile devices).

The script was tested before and after compilation to avoid problems with action.

The "YouLinux" script is written for the GNU/Linux environment. It was tested on several Linux distributions (Kali, Ubuntu, Parrot, Mint...) on different kernel versions.

>[!WARNING]
> The script does not work properly on Ubuntu and Ubuntu-based systems.
>
> Unfortunately, I was not able to get to why this is happening.
>
> Due to the fact that by default I mainly write scripts for Termux, I will not work on repairing this problem.

>[!CAUTION]
> If the script action looks incorrect or suspicious, DO NOT RUN IT!!!

The script was tested before and after compilation to avoid problems with action.

### YouTube age limitations:

The script has implemented features and flags `-c` | `--cookies` that allow script to use YouTube cookie files of the selected browser. This allows logged in users to download content with applied age restrictions.

>[!NOTE]
> To use this option, the user must be logged in to YouTube in a selected browser.

### Errors:

+ The script does not work properly on Ubuntu and Ubuntu-based distros.

+ Downloading a list of titles can digest a long time.

+ The script does not check the correctness of the input data. It can end the work with an error if you enter `-u`, `-up`, `-f` parameters incorrect.

+ The script will stop downloading files correctly if there are more than 100 when using the flag `-o` | `--output`.

### Version:

The current version of the script is "1.0 beta", which means that this is the first and test version of the script.

It is possible to appear additional errors that I could not notice or reproduce in my environment.

![screenshot](/version.jpg)

>[!CAUTION]
> If the script action looks incorrect or suspicious, DO NOT RUN IT!!!

## Support ...

### Contact:

In case of any problems, irregularities, suggestions and questions, please contact me:

+ Email : **support@burixon.com.pl**

+ Contact form : **[click here](https://burixon.com.pl/kontakt.php)**

### Support me:

I write useful and simple life tools to make life easier. If you consider this script and the others to be useful and helpful, you can let me know about it by paying tip on my website: **[DONATIONS](https://burixon.com.pl/donate/)**.

This should help me in further development, creating new projects, scripts and programs.

The Termux and Linux environment is made up of users. Your contribution to my work can help us develop them all!
