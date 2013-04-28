#Editing and Creating a markdown based PDF#
###By Heather Dykstra##
####With Additions from Andrea Sassu and Hannah Thomas####

#Option 1: Python Script

Intial source for general help: http://www.reddit.com/r/LaTeX/comments/1cyc14/presentation_with_beamer_file_help_needed/


If you like the idea of the pdf-presenter-console you MUST install/run it on ubuntu (so our virtual boxes will work fine). This feature allows for a timer to run on your main comp while you present and shows how much time you have left. It is really cool but the software isn't as functional as I would like it to be. I emailed the guy behind it, so we shall see if that goes anywhere. *crosses fingers*

If you decide to use my beamer and generate, PLEASE change the color or text or theme (just because I spent a lot of time getting it to work and I am really happy with what I have now, and Its really easy to change.)
(You must also change the content of the .md file, most of that is just garbage right now anyway)

Potential colors/fonts/themes are found here:
 
 http://deic.uab.es/~iblanes/beamer_gallery/individual/AnnArbor-wolverine-structurebold.html
 
##CHANGE THE FONT OR COLOR:##
Just edit the talk.beamer file (below are the first 6 lines where the edit needs to be made):

> \documentclass[$if(fontsize)$$fontsize$,$endif$$if(handout)$handout,$endif$$if(beamer)$ignorenonframetext,$endif$]{$documentclass$}

>$if(theme)$

>\usetheme{$theme$}

>$endif$

>\usecolortheme{beaver} %Change this if not in Heather's group

>\usefonttheme{structuresmallcapsserif} %Change this if not in Heather's group

##CHANGE THE THEME:##
you can also edit line 13 in generate

>pan_args = ["pandoc", "-f", "markdown", "-V", "theme:Dresden"]

>and change "theme:Dresden" to whichever theme you liked from the above website. 

##OTHER INFO:##
I included everything you really need as a final slide in my pdf (slide 21) (it is also at the bottom of the .md file)

Note that if you change the name of any file you have to change it everywhere it is called.

I think there were a few other small dependencies that i may have had to install to get generate to work, but I think that is explained in Baker's readme. 

#Option 2: Shell Script
**(by Hannah Thomas)**

A simple shell script capable of running on Macs, and most likely Windows and Ubuntu (haven't tested it yet), is also available.

It is very simple to use and still allows for editing the theme and color scheme (and I plan to add font later). Instructions are provided in the *README* within the *Simple Slideshow Generator for Mac* folder.

##ADOBE READER FOR TIMING##

*The following section was later added by Andrea Sassu*

If you have Adobe Reader and the presentation generated into a .pdf before your time to present, then you can just 
use the fullscreen settings for Adobe Reader. 

All you have to do go to __Edit -> Preferences -> Full Screen__, and there 
should be an option to __"Advance every _ seconds."__ If you just put 15 in the time field, and put the presentation 
in fullscreen mode at the start of your presentation, then you should be good to go!

-----------------------------------------------------
