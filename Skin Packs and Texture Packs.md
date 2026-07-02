# Making Skins/Textures on Minecraft LCE
Mainly for the Source Code Leak. Written by IveBeenAlone (IBA).

# Section 1 - Required Programs

Firstly, you are going to **need** the following,

- PCK Studio (https://github.com/LCERD/PCK-Studio/releases/latest)

Secondly, you will probably want one (or more) of these.

- PaintDotNet (or any other art/paint that has transparancy) (https://paint.net/)

- Blockbench (if you want custom models) (https://www.blockbench.net/)

- Minecraft LCE Toolkit (used for mainly \*.arc files)
(https://github.com/RhysEvoo/Minecraft-LCE-Toolkit/releases)

- JPEXS Decompiler (used to edit swf files that can be found in \*.arc
files) (https://github.com/jindrapetrik/jpexs-decompiler/releases)

- MLCE Texturepack Builder (entirely optional, but recommended if
making texture packs)
(https://github.com/romrom83/MLCE-texture-pack-builder/releases)

# Section 2 - Basic Skins

So, to make a skin (or skin pack), you will want to open your root
directory, this is where the games .exe file is. If you are using a
launcher like Emerald and on windows, this will be in
**`%localappdata%\\com.emerald.legacy\\instances`**.
You want to navigate to Windows64Media\\DLC, and make a copy of Skin
Pack 1. You do NOT have to do this if you are replacing skins, but keep
in mind if you replace a skin, it will only show for you.

Once you have made this copy, rename it to whatever you want the Skin
Pack Display Name to be in game.

Once you have done that, open the folder and PCK Studio. You will want
to drag and drop the copied PCK file onto PCK Studio, or go File \> Open
and select the copied PCK file. Once you have done that, you will be
given something that looks like this,

As you can see, dlcskin######## are the skins in Skin Pack 1. You can
click on the files to see the skin texture. But we aren't interested in
any of that. What we want to do is click one, and hold our delete key
(or right click > delete) until all but one is gone. Why all but one?
PCK Studio doesn't update and show newly added files all the time
otherwise, we will delete the last one once we have made our skin. Once
we have done that, we want to right click where the skin files used to
be and select Create > Skin. You will be presented with something like
this,

What you want to do is click "Edit Skin Flags", and UNCHECK "64x64
Classic Skin". Unless your fork has 64x64 skin support, you WILL have
to uncheck this!!! (Forks here include Console editions, such as X360.)
It should look like the following,

Again, this is to make a basic Steve skin, enable and disable what you
know your fork supports. If your unsure, you can always try it and
change it later! Once we have done that, click Save, and that window
will close. Now, we want to select "Auto-Gen" for our Skin ID, if you
know how this works, you can skip this and assign your own ID. A quick
summary is that, every skin has its own unique 8 digit ID. I have
personally used more than 8 digits, but I do not know if it is safe to
do so.

After selecting Auto-Gen, give your skin a name, and a theme name, These
will show up here!

Now lastly.. The skin. You are going to want to click anywhere in this
box and select your skins png file. Remember! If your fork does NOT
support 64x64 skins, you will have to use a 64x32 skin file.

In some forks you CAN use higher resolution skins via a loop-hole of
sorts. Minecraft LCE doesnt look at the size of the skin, it looks at
ratio, so a 2:1 skin or a 1:1 skin. So you can use a 128x64 skin instead
of a 64x32 skin. This will NOT give you more model/layers, this will
just make your skin higher quality.

You can also optionally add a cape texture,

But it's not required. When you've selected your skin of choice, click
"Create Skin". Repeat this for as many skins as you want to make!

When you are done adding your skins, go File > Save As.. And find the
skin folder we originally copied. We *can* leave the PCK File named
Skins1.pck, but we should name it something related to the pack itself.
If you do choose to rename the PCK file, delete the originally copied
Skins1.pck

And lastly, boot up LCE and see if it's in the game. If not, make sure
everything is properly done, as this should have made a working basic
Steve model skin.

# Section 2 - Advanced Skins

To make more advanced skins, ones with custom models and such, you will
want to use Blockbench and make the model/skin file. This is your job to
include the bbmodel and skin texture I send you neoapps.

You don't need the full downloaded version of blockbench, the web
version works perfectly fine for this. But you *may* want the web
version if you are making these kind of skins regularly, or porting
stuff from Bedrock, but that's a kinda different thing. If your able to
follow this and make a custom skin here, you'll be able to port a
Bedrock skin by yourself.

So, you want to follow Section 1 until you get to the part about
choosing your skin texture. Instead of doing that, we want to click on
"Edit Model", and select "Yes"

After a moment, we will get this,

When this opens, we want to select "Import Skin", like the image above
shows.

When we do PCK Studio will warn us that our work will be lost, but thats
fine, as there is no work yet. So this is safe to ignore and click on
Yes. A file selecter window will open up, in the bottom right we want to
change the selection from PCK Studio Model files, to bbmodel files, as
well as navigate to your models saved bbmodel file and open it.

The model *may* appear invisible, I don't know why it does this, but
hit create anyways. When that's done, follow the rest of the basic skin
guide. you **may** need to reselect the correct skin flags, or
depending on your model, enable some to hide its armour or Steve models
body parts.

# Section 3 - Textures (simple)

For texture packs, the same idea applies, copy a texture pack folder,
rename, and open the pck file. What differs however, is how the file is
made.

For this simple methood we are going to use romrom83's
MLCE-texture-pack-builder. As it's a lot easier and simpler than
editing a pre-existing pack. You are going to want both the
template_pack_minecraft_consoles.zip and template_pack_MCLE.zip. Unzip
these where ever you want them, but keep them close to each other as
youll need both. Open up the template folder and replace/edit the files
as you need. You can use Common\\res\\\* to view every texture LCE
supports, and where they should be. Texture packs do NOT use 1_2_2 or
TitleUpdate folders. If a texture is in res\\TitleUpdate\\res\\mob, it
should just be in res\\mob in your texture pack.

Once all that is done, open up TexturePackBuilder.exe choose your source
folder, it should be the one with the README.txt in it. Give your pack a
name, an ID, and a description, and pick the resolution. Unless you are
manually making a texture pack (described in Section 4), you are limited
to 16x or 32x.

When those are filled out, hit Convert! It should make a new folder at
where ever you put TexturePackBuilder.exe\\output\\\[packname\]. You
should just be able to now copy the pack name folder into your DLC
folder. Simple as that!
