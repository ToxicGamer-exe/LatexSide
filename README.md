# WARNING - This is WiP, it was just quickly written from what I remember I used. I'm gonna test everything out once again from the start, so I'm gonna update everything later on. If you're gonna use any of the run scripts, don't forget to change the paths!

# LatexSide
Tutorial for implementation of Latex into Writerside

I made this since I'm sick of relying on either old Latex editors or having to pay for one. So I randomly found Latex package for Jetbrains IDEs and decided to give it a shot. Sadly there are basically no tutorials at this time, so you're all by yourself. When I finally made everything somewhat stable, I decided to help others (and myself in the future) till I remember it. Hopefully it's gonna help you overcome the worst issues, if not, feel free to address them into Issues.
I should also mention that this is Mac oriented, I didn't test it on Windows yet, but hopefully it's gonna work similarly (or it might be even easier). I apologize for any unnecessary/weird steps, I'm completely new to MacOS (bought it for Christmas couple days ago), so I did a lot of things with "trial and error" method. I'm gonna update this tutorial, but for now, I'm just glad its stable :D.

# IDE Plugins
- I suppose you already have Writerside downloaded (Or any other Jetbrains IDE), so I'm not gonna walk you through that
- As you probably know you can download it right in IDE. Go to the **Settings(`Cmd+,` or `Ctrl+Alt+S`)>Plugins** and in the Marketplace tab, find the wanted plugin in the search bar. **Install** it and don't forget to **restart** your selected IDE if the installation requires it.

### TeXiFy
- First (easiest) thing you wanna do is download this awesome plugin called **[TeXiFy](https://plugins.jetbrains.com/plugin/9473-texify-idea)**

### PDF Viewer
- For quick viewing of PDFs in IDE
- Recommended by TeXiFy authors, but there are other options to choose from

### Shell Script
- For running scripts in run configs.

# MikTex
- A pack of all the latex tools/compilers you might need
- Compatible with most used OS (Win/Mac/Lin)
- Just choose the right OS [here](https://miktex.org/download) and download it (Further info in tutorials they provide)
- Once everything is downloaded, you have to upgrade it to the full version, otherwise it won't work...
- It also provides downloading packages "on the fly" (automatically during compilation), I personally recommend setting it to Always (in Settings)

# BasicTex/MacTex
- Something like MikTex, but more recommended for Mac users. I experimented with both (so I have both downloaded), but I think you should be able to get around without it.
- Sadly MacTex is really big compared to MikTex. That's where BasicTex comes in play.
- BasicTex is just small version of MacTex (without editor and other stuff you don't really need), but still containing all the essentials.

# TexLive Package Manager
- Should be provided by your chosen Latex distribution
- Tool for installing/updating Latex packages manually
- Make sure you have it updated with `tlmgr update --self`
- You can install packages with `tlmgr install *package name*` and update with `tlmgr update *package name*` (--all instead of package name to update everything --list to see all updates for packages)

# TexLiveOnFly
- Solves all your package problems by automatically downloading them during compilation
- You can easily download it with `tlmgr install texliveonfly` or from [GitHub repo](https://github.com/maphy-psd/texliveonfly)
- Make sure you have downloaded python
- Look on the [GitHub repo](https://github.com/maphy-psd/texliveonfly) for usage, or just use my run script

# LatexIndent
- Last thing missing is something for code formatting
- If not provided by your Latex distribution, you can install it just like previous package with `tlmgr install texliveonfly`
- You can use my run scripts (if you don't have main.tex in the root or it has different name, don't forget to update their paths)
- There is also my indentconfig.yaml that you can use for further customisation, just put it in home directory and change the path in the config.
- [GitHub repo](https://github.com/cmhughes/latexindent.pl) | [Documentation](https://latexindentpl.readthedocs.io/en/stable/)

- Config descriptions / Custom settings
- Brew/Perl?
- (Custom language support?)
- (Github?)

# Common Issues
### Pdflatex doesn't work
If your pdflatex doesn't compile, make sure you have downloaded it with one of the **"Tex" apps** and that you have provided the right path to the script in the **Latex** run configs.

### TexLive doesn't work
Ensure you have python installed and that you call it with the right python.

### LatexIndent script doesn't work
Please make sure you have downloaded pcre. If not, install it with `brew install pcre`. if still nothing, make sure you have your indentconfig.yaml in the right (home) directory (which you can also find in the defaultConfig.yaml + on the start of the script) and you have provided the right path in it.

### LatexIndent doesn't format
If you used my latexindent config, but have your own run script, don't forget to run it with the -m option, otherwise the script isn't allowed to change lines. You also need --overwrite option for the script to overwrite the current file. If you are using my run script, make sure you provided the right paths to it.
