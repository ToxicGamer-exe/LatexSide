# LatexSide
Tutorial for implementation of Latex into Writerside

I made this since I'm sick of relying on either old Latex editors or having to pay for one. So I randomly found Latex package for Jetbrains IDEs and decided to give it a shot. Sadly there are basically no tutorials at this time, so you're all by yourself. When I finally made everything somewhat stable, I decided to help others (and myself in the future) till I remember it. Hopefully it's gonna help you overcome the worst issues, if not, feel free to address them into Issues.
I should also mention that this is Mac oriented, I didn't test it on Windows yet, but hopefully it's gonna work similarly (or it might be even easier). I apologize for any unnecessary/weird steps, I'm completely new to MacOS (bought it for Christmas couple days ago), so I did a lot of things with "trial and error" method. I'm gonna update this tutorial, but for now, I'm just glad its stable :D.

# TeXiFy
- I suppose you already have Writerside downloaded (Or any other Jetbrains IDE), so I'm not gonna walk you through that
- First (easiest) thing you wanna do is download this awesome plugin called **[TeXiFy](https://plugins.jetbrains.com/plugin/9473-texify-idea)**
- As you probably know you can download it right in IDE. Go to the **Settings(`Cmd+,` or `Ctrl+Alt+S`)>Plugins** and in the Marketplace tab, find TeXiFy. **Install** it and don't forget to **restart** your selected IDE if the installation requires it.

Topics left:
- MikTex
- BasicTex/MacTex
- PDF Viewer
- Shell Script
- TexLiveOnFly
- LatexIndent
- Config descriptions / Custom settings
- (Custom language support?)
- (Github?)

# Common Issues
### Pdflatex doesn't work
If your pdflatex doesn't compile, make sure you have downloaded it with one of the **"Tex" apps** and that you have provided the right path to the script in the **Latex** run configs.

### LatexIndent script doesn't work
Please make sure you have downloaded pcre. If not, install it with `brew install pcre`. if still nothing, make sure you have your indentconfig.yaml in the right (home) directory (which you can also find in the defaultConfig.yaml + on the start of the script) and you have provided the right path in it.
