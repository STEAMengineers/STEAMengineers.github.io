---
layout: post
title:  "Making A Simple Character"
date:   2025-02-19 07:00:00 +0000
---
Chris is working on a post about PCB creation, but Chris is also working on 700 other things. So while we wait for that, I thought I'd share a little shortcut I sometimes use to make quick illustrations. It's only one of many ways I make pictures (I also draw and paint both analog and digital pictures, and sometimes mix the two) but maybe it'll help someone who's a bit stuck. As [Michael Dales](https://mastodon.me.uk/@michael@mynameismwd.org) (sorry to link to his mastodon, but he does so many incredible things I couldn't pick a website) pointed out, sharing is a radical act in a society where everything turns on marketability and monetisation.

So here we go. You want to make a simple image - these are especially helpful when you're making content of any type for kids, for example. For the sake of my reputation, let's call it a little robot face.

I start in [Inkscape](https://inkscape.org/) (as is the case with most of my digital projects other than paintings), and make a simple little robot face:

![image](https://github.com/STEAMengineers/STEAMengineers.github.io/blob/main/assets/images/for%20blog%20posts/robot%20face.png?raw=true)

(Image ID: a happy-looking, very simple robot face in black lines on a white background. End ID.)

Don't forget you can change shapes easily enough - I rounded my rectangle's corners evenly by pulling down on the round handle once I'd drawn the rectangle. Similarly, a circle can easily be turned into part of a circle (or a little Pacman) by using that round handle. A little grouping for the eyes, a little aligning, 2 minutes later we have a little robot. Some drawings, and especially lasercutting files, need paths to interact - if you're not very familiar with Inkscape, definitely play around with that a bit. You can't break anything by having a file with some shapes and combining them in various ways :)

Saving this robot face as a .xcf allows me to open it in [GIMP](https://www.gimp.org/) with a fully transparent background - which helps a lot when all you actually want is the linework. Open it in GIMP and crop the image if necessary (my default Inkscape document size is 600x400mm to coincide with my lasercutter). We're now here:

![image](https://github.com/STEAMengineers/STEAMengineers.github.io/blob/main/assets/images/for%20blog%20posts/robot%20face%20transp%20bg.png?raw=true)

(Image ID: the same black linework, now on a dark- and light-grey chequerboard pattern signifying a transparent background. End ID.)

Quick note: If you want to perfectly centre your object in the final image, you can draw another rectangle outside of it, and use the alignment tool to centre it within that. Once in GIMP, **Image &gt; Crop to Content**, and you're golden. If you want to get rid of the outer rectangle, simply select all, then **Select &gt; Shrink...** and shrink your selection by however many pixels will cut out the outer rectangle you used for alignment. **Image &gt; Crop to Selection** - problem solved :)

Add a layer, place it below your original layer, and - I cannot emphasise this enough - **name your layers**. It's not maybe necessary for something quick and dirty like this, but it's the most valuable habit you can form if you use layers in whatever you're making. Name your layers and stick to those names. In this case, I'd name mine "lines" and "colour" for simplicity, but I have more complex paintings that have upwards of 20 layers, down to things such as "shiny bit for x component." If you don't name the layers, you're going to lose track really quickly (which will absolutely still happen if you do name them, but I can only save you from so many agonies).

Now you can use the Fuzzy Select tool (looks like a magic wand with a star at the end) on your "lines" layer to select regions. For example, select inside of the face - or select inside one eye, hold Shift, and select inside the other eye (to remove selected areas from a group, hold Ctrl). Now move back to your "colours" layer to colour these areas.

Immediately, a problem occurs. If you zoom in after filling those selected regions on your "colours" layer, you can see it doesn't work perfectly:

![image](https://github.com/user-attachments/assets/60eabf7e-6a96-42a2-b32d-55dd8e1c478a)

(Image ID: a close-up of the line making up the top of one of the eyes. The eye is filled with a bright blue - other than the linework, the rest of the image contains the light- and dark-grey chequerboard denoting transparently. Some transparent pixels are clearly visible between the black line and the blue fill. End ID.)

As you can see, some pixels were left out. There's an easy fix for this; in the **Select** menu, you can pick **Grow...** How many pixels you grow your selection by depends on the thickness of your lines - in this example, I've grown by 2 pixels. As you can see, once I fill this new selection (on the "colour" layer), it fills properly and doesn't leave any naked little pixels.

![image](https://github.com/user-attachments/assets/31d1b9ea-8e76-482c-9693-4c631f0171d2)

(Image ID: two screenshots, one above the other. The top one shows the eye of the robot, selected in such a way that the outer line of the selection sits below the line. The bottom image shows the eye perfectly filled in bright blue. End ID.)

Now use the same technique to add some depth to the eyes, and colour in the other elements of your drawing. 

![image](https://github.com/STEAMengineers/STEAMengineers.github.io/blob/main/assets/images/for%20blog%20posts/robot%20face%20coloured.png?raw=true)

(Image ID: a happy robot face, now completely coloured in. The background is still transparent, but the face has a shiny grey colour, with blue eyes and a dark red mouth. Each element has some amount of shadow, and the eyes and face have shinier bits at the top. End ID.)

Simple. Fill in your background however you like, and you're done. 

Again, this is very quick and dirty, for simple images. You can make this as complex as you like - I sometimes scan line drawings I've done on paper, and mess around until I can use that drawing as linework, or I make more complicated shapes, or I draw directly into GIMP or [Krita](https://krita.org/en/). Or sometimes, my lines are really just a sketch and I put my colours in a layer on top, because they won't be visible at the end. Your only real constraint is how much time and energy you have.

Sometimes I use my drawing tablet, but everything in this particular post has been done using only the trackpad on my laptop. You don't need expensive or complicated equipment, and the undo button is your friend - if you're unhappy with a stroke, just undo and try again until you are! Perfection is the enemy of done, that is very true. But there's a sneakier, more insidious idea that **if it's not right on the very first try, that means you're bad at it and should stop trying.**

Nothing is further from the truth. Every wrong line fills in some of your map to the right one. And everyone you know who creates things you think you can't match, is drawing the wrong lines on a regular basis. Just stick with it, and hang around for Chris's post about the PCB side :)
