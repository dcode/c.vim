README for c.vim (Version 5.19) // 2012-05-18

  *  DESCRIPTION
  *  INSTALLATION
  *  RELEASE NOTES 
  *  FILES
  *  ADDITIONAL TIPS
  *  CREDITS

=======================================================================================
  DESCRIPTION
=======================================================================================
C/C++-IDE for Vim/gVim. It is written to considerably speed up writing code in
a consistent style.  This is done by inserting complete statements, idioms,
code snippets, templates, and comments.  Syntax checking, compiling,  running a
program, running indent or code checkers can be done with a keystroke.  There
are many additional hints and options which can improve speed and comfort when
writing C/C++. See the help file csupport.txt for more information.

=======================================================================================
  INSTALLATION
=======================================================================================
The subdirectories in the zip archive  cvim.zip  mirror the directory structure 
which is needed below the local installation directory $HOME/.vim/ for LINUX/UNIX
($VIM/vimfiles/ for Windows; find the value of $VIM with ":echo $VIM" from inside Vim).

(0) Save the template files in '$HOME/.vim/c-support/templates/Templates' if
    you have changed any of them.

(1) Copy the zip archive cvim.zip to $HOME/.vim and run

      unzip cvim.zip

    If you have already an older version of cvim and you have modified the template
    files you may want to save your templates first or copy the files from the 
    archive by hand.

(2) Loading of plugin files must be enabled. If not use

      :filetype plugin on

    This is the minimal content of the file '$HOME/.vimrc'. Create one if there
    is none. 

(3) Set at least some personal details in the file '$HOME/.vim/c-support/templates/Templates'
    (file '$VIM\/c-support/templates/Templates' under Windows). 
    Here is the minimal personalization (my settings as an example, of course):

      |AUTHOR|    = Dr. Fritz Mehner 
      |AUTHORREF| = mn
      |EMAIL|     = mehner@fh-swf.de
      |COMPANY|   = FH Südwestfalen, Iserlohn
      |COPYRIGHT| = Copyright (c) |YEAR|, |AUTHOR|

    (Read more about the template system in the plugin documentation)

(4) Consider additional settings in the file '$HOME/.vimrc'.
    The files customization.vimrc and customization.gvimrc are replacements or 
    extensions for your .vimrc and .gvimrc ( _vimrc and _gvimrc under Windows).
    You may want to use parts of them. The files are documented. 

There are a lot of features and options which can be used and influenced:

  *  use of template files and tags
  *  surround marked blocks with statements
  *  using and managing personal code snippets
  *  generate/remove multiline comments 
  *  picking up prototypes
  *  C/C++ dictionaries for keyword completion
  *  (re)moving the root menu

Restart gVim/Vim generate the help tags  

  :helptags ~/.vim/doc

and look at csupport help with

  :help csupport 

or use the 'help' item in the root menu of this plug-in.

             +-----------------------------------------------+
             | +-------------------------------------------+ |
             | |    ** PLEASE READ THE DOCUMENTATION **    | |
             | |    Actions differ for different modes!    | |
             | +-------------------------------------------+ |
             +-----------------------------------------------+

Any problems ? See the TROUBLESHOOTING section at the end of the help file
'doc/csupport.txt'.

=======================================================================================
  RELEASE NOTES FOR VERSION 5.4
=======================================================================================
+ New hotkey \+co inserts ' cout	<<  << endl;'
+ New menu item C++-menu: 'cout' replaces 'cout variable' and 'cout string'.
+ Hotkey \c/ removed ( \cc does the same).
+ Bugfix: after an unsuccessful compilation screen sometimes garbled.

  OLDER RELEASE NOTES : see file 'ChangeLog'
=======================================================================================

=======================================================================================
  FILES
=======================================================================================

README.csupport                 This file.

doc/csupport.txt                The help file for the local on-line help. 
                          
ftplugin/c.vim                  A file type plug-in. Define hotkeys, creates a local 
                                dictionary for each C/C++ file.

plugin/c.vim                    The C/C++ plug-in for GVIM.

c-support/scripts/wrapper.sh    The wrapper script for the use of an xterm.
c-support/templates/*           C-style and C++-style template files (see csupport.txt).


c-support/wordlists/c-c++-keywords.list   All C and C++ keywords (already in word.list).
c-support/wordlists/k+r.list              K&R-Book: Words from the table of content. 
                                          They appear frequently in comments.
c-support/wordlists/stl_index.list        STL: method and type names.


-----------------------   -------------------------------------------------------------
                          The following files and extensions are for convenience only.
                          c.vim will work without them.
                          -------------------------------------------------------------
c-support/doc/c-hotkeys.pdf  Hotkey reference card.
c-support/doc/ChangeLog      The change log.

rc/customization.ctags       Additional settings I use in  .ctags to enable navigation
                             through makefiles ans qmake files with the plug-in taglist.vim.

rc/costumization.gvimrc      Additional settings I use in .gvimrc :
                             hot keys, mouse settings, ...
                             The file is commented. Append it to your .gvimrc if you like.

rc/costumization.indent.pro  Additional settings I use in .indent.pro :
                             See the indent manual.

rc/costumization.vimrc       Additional settings I use in .vimrc :  incremental search,
                             tabstop, hot keys, font, use of dictionaries, ...
                             The file is commented. Append it to your .vimrc if you like.

=======================================================================================
  ADDITIONAL TIPS
=======================================================================================

(1) gVim. Toggle 'insert mode' <--> 'normal mode' with the right mouse button
    (see mapping in file costumization.gvimrc).

(2) gVim. Use tear off menus.

(3) Try 'Focus under mouse' as window behavior (No mouse click when the mouse pointer 
    is back from the menu item).

(4) Use Emulate3Buttons "on" (X11) even for a 3-button mouse. Pressing left and right
    button at the same time without moving your fingers is faster then moving a finger
    to the middle button (often a wheel).

=======================================================================================
  CREDITS
=======================================================================================

  Some ideas are taken from the following documents:

  1. Recommended C Style and Coding Standards (Indian Hill Style Guide)
      www.doc.ic.ac.uk/lab/secondyear/cstyle/cstyle.html
  2. Programming in C++, Ellemtel Telecommunication Systems Laboratories
      www.it.bton.ac.uk/burks/burks/language/cpp/cppstyle/ellhome.htm
  3. C++ Coding Standard, Todd Hoff
     www.possibility.com/Cpp/CppCodingStandard.html

  The splint error format is taken from the file splint.vim (Vim standard distribution).  

------------------

  ... finally

  Johann Wolfgang von Goethe (1749-1832), the greatest of the German poets,
  about LINUX, Vim/gVim and other great tools (Ok, almost.) :

    Ein Mann, der recht zu wirken denkt,         Who on efficient work is bent, 
    Muß auf das beste Werkzeug halten.           Must choose the fittest instrument.  

  Faust, Teil 1, Vorspiel auf dem Theater      Faust, Part 1, Prologue for the Theatre 

=======================================================================================
