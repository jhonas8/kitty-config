# My Kitty terminal emulator settings #
## This is my kitty terminal emulator configuration. I've started using it recently, so there's not a lot yet. ##

<img
    alt="Print kitty-terminal"
    src="./.git-assets/kittyPrint.png"
/>  

[<img
    alt="Kitty icon"
    src="https://sw.kovidgoyal.net/kitty/_static/kitty.svg"
    width="22px"
    align="left"
/>][kitty-link]
Access Kitty's documentation!

## Theme ##

**The theme being used is part of a theme package available on [Github][theme-package].**

The current theme is the **WarmNeon**. The color palette is:  
   
    background            #3f3f3f
    foreground            #afdab6
    cursor                #2fff24
    selection_background  #b0ad21
    color0                #000000
    color8                #fdfcfc
    color1                #e24345
    color9                #e86f71
    color2                #38b139
    color10               #9bc08f
    color3                #dae145
    color11               #ddd979
    color4                #4260c5
    color12               #7a90d5
    color5                #f81ffb
    color13               #f674b9
    color6                #29bad3
    color14               #5ed1e4
    color7                #d0b8a3
    color15               #d8c8bb
    selection_foreground  #3f3f3f

##### For implementing it on your terminal, you can simply paste it on your **kitty.conf** or paste it on a separate file and include it on there. ##### 

In this case, I've created a link to a file containing the collor palette from the source path. You can do it by running the following code:  

    ln -s ./kitty-themes/themes/<ThemeName>.conf ~/.config/kitty/theme.conf 

By running this, you create a link for the file <ThemeName>.conf and name this link as 'theme.conf'.  

Now you need to import it into your **kitty.conf** file, by running:

    include ./theme.conf

__Notice I'm considering you named the link as theme.conf__

## Key mappings ##

Notice I'm using **native_code** for mapping the keys.

### Next tab ###
Using CTRL + K for switching to next tab:  

    map ctrl+0x6a previous_tab

### Previous tab ###
Using CTRL + J for switching to previous tab:

    map ctrl+0x6b next_tab

### Open new tab in the same directory ###
Using F1 to open a new tab in the same directory as the current tab:

    map 0xffbe new_tab_with_cwd

## Terminal Styles ##
### Fonts ### 
I'm using [Fira Code][fira-code] font. Font-ligatures are automatically compatible to Kitty. The font size was set to 16px.

    font_size 16.0
    font_family FiraCode

It will only work if Fira Code is installed on the machine. 
If you **DON'T** want the font-ligatures, you can add the follwing line:

    font_features FiraCode -liga 

The `-liga` will disable normal ligatures. There's also `(+/-)calt` feature (in Fira Code) which allows breaks up monotony.

## Tab Separator ##

    tab_separator " ???"
    tab_bar_style powerline

And you have this result as for the terminal tabs:
<img
  alt="tab separator"
  src="./.git-assets/tabSeparator.png"
/>

## Launching flags ##
As for the lauching flags, I set the background opacity to 0.95 (95%). That's the only flag I use and you can do it by running the following command in your terminal:

    kitty -o background_opacity=0.95

#### I also setted up the command above to run by pressing the CTRL+ALT+t. In my case, I used the native Gnome 3 keyboards-shortcuts to set it up. If you're using the same interface, you can do it by following the steps: ####

#### Step 1 ###
<img
    alt="step 1"
    src="./.git-assets/step1.png"
/>

### Step 2 ### 
<img
    alt="step 2"
    src="./.git-assets/step2.png"
/>

### Step 3 ###
<img
    alt="step 3"
    src="./.git-assets/step3.png"
/>

## Synth Shell ##
The fancy shell initialization is called Synth shell and you can easily install by following the steps on its documentation. 
[<img
    alt="synth-shell"
    src="https://raw.githubusercontent.com/andresgongora/synth-shell/master/doc/synth-shell.jpg"
    width="40px"
    align="right"
/>][synth-shell]  
  
<img
    alt="synth-shell print"
    src="./.git-assets/synth-shell.png"
/>

[theme-package]: https://github.com/dexpota/kitty-themes
[kitty-link]: https://sw.kovidgoyal.net/kitty/
[fira-code]: https://github.com/tonsky/FiraCode
[synth-shell]: https://github.com/andresgongora/synth-shell
