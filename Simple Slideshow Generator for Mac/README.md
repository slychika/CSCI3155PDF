#Simple Slideshow Generator for Mac
**By Hannah Thomas**

##Notes
I plan to add the timer functionality as soon as I figure out how to.

This generator assumes that your slide titles are made using the second header formatting (## or ----). If you would like to use something else, either delete the `--slide-level=2` part or place in another number for `slide-level`.

Also, I think this should work on Windows and Ubuntu, but am not entirely sure.

##Instructions

So, I had issues using the python script to make a PDF, so I made my own shell script.

###Necessary Software:

1. [Pandoc](https://code.google.com/p/pandoc/downloads/list) *(Any OS)*
2. [MacTex](http://tug.org/mactex/) or [BasicTex](http://tug.org/mactex/morepackages.html) *(Mac Specific)*

###Running the Shell Script

1. Put the shell script in the same place as your markdown file.
2. Edit the shell script so that `"Paper Slideshow.md"` is your markdown file. Quotes are only needed if there is a space in the name. You can also change the current output file (slides.pdf) to whatever name you would prefer.
3. Open the terminal and type `chmod 755 makebeamer.sh`. You should only have to do this once.
4. Just type `./makebeamer.sh` to run the script!

###Changing the theme
1. Open shell script.
2. Where the script says `theme:Antibes` place an [appropriate theme](http://deic.uab.es/~iblanes/beamer_gallery/index_by_theme.html).
3. Where the script says `colortheme:seahorse` place an [appropriate color theme](http://deic.uab.es/~iblanes/beamer_gallery/index_by_color.html).
4. Mix and match to your heart's content!


