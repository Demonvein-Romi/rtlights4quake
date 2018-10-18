# rtlights4quake
A collection of .rtlights and cubemaps for Quake engines that support real-time lighting files. 

## HOW TO
Getting .rtlights to work is a fairly straight forward process but requires a few steps.

## FILES
The first item you will need is the Quake 1 .pak files, they contain the raw data for the game. If you purchase Quake on steam or some other platform you should be able to find the files.

The two paks are called PAK0.PAK and PAK1.PAK.

In base install mode they should reside in quake/id1/

If you so desire you can always keep them in there, or you can move them to a new folder if you plan on altering them (re-vis for example).

The next item you will need is a .rtlight supporting Quake engine, such as Darkplaces or FTE QW.

Despite the website being dated, the Darkplaces engine project continues and gets regular updates. Although there are more recent builds, currently the most stable build I have found is one from April 2018. It can be found [here](https://icculus.org/twilight/darkplaces/files/darkplacesengine20180412beta1.zip).

FTE QW can be found at http://fte.triptohell.info/

The Darkplaces or FTEQW executable should go in your '/quake' folder.

The next item required will be the .rtlights themselves, take the .rtlights files and place them in the id1/maps/ directory. The cubemaps folder should be placed in your 'quake/id1 directory' if you wish to use those, or if you wish to use specific cubemap image files they should be placed in the 'quake/id1/cubemaps/' directory. 


## VISING YOUR ID1 MAPS
Now that you have all the files you need the next step is to re-vis your maps. This process can be fairly annoying, but there are fortunately some easier ways to accomplish it using existing vis data and using that instead of re-compiling maps. You can get everything you need for that process [here](http://vispatch.sourceforge.net/).

Once you have your maps properly vis’d launch Darkplaces and turn on real-time lighting, the option can be found in the game menu by going to Options > Customize Lighting > RT World > On . You can also go into the console by hitting ~ and typing r_shadow_realtime_world 1

That is it, play around with brightness and graphics until you are happy and start playing.

## GRAPHICS OPTIONS (DARKPLACES ONLY)
A few settings you may want to mess with:

For that old school software quake texture feel go to the console ~ and type gl_texturemode gl_nearest

For some interpreted bumpmap effects on the stock textures go to the console and use the command r_shadow_bumpscale_basetexture 4-5. Be sure type in r_restart in the console to enable this change, as it requires the render to reload in order to work.

You can always turn on gloss and coronas as well in the menu, but I personally don’t recommend those effects. If you wish you can also download mysettings.cfg and type "exec mysettings.cfg" in the console. This will put the relevant graphics settings to the same I use for my editings, playthroughs, and screenshots. 

## EDITING .RTLIGHTS
If you want to play around with the lights themselves type in r_editlights 1 into the console.

If you are curious about more functions you can always type the start of a command and hit tab, it will show you all the options and a brief explanation of what they do, this is important for .rtlight editing, even after doing this for years I still find myself typing r_editlights_ and hitting the tab key to see all the options. You can also use the apropos command to search for any command using the string entered, for example "apropos shadow" 
