# GameDevelopmentLinks
This is a collection of useful game-development links including, but not restricted to, development with MonoGame.

During the process of developing our game I came across a large variety of websites that I found very useful.  
This page is a collection of all of them baring a short description. I will check in every month or so and update this list accordingly.  
Let me mention that I didn't record those links in any particular order and that the sites, I link to in this section, may contain much more than the description of the link suggests. Chances are that I didn't even look through each and every page of every single site before finding it helpful and bookmarking it. These are just the pages I found searching for solutions for the problems in the various fields of interest you inevitably stumble over when starting to write a game.  
  
I tried to sort every link-table it in a way that should benefit your learning curve (most complex subjects last).  

If you want to contribute just fork this repo, make changes and then a pull request.
Contributions are welcome!

# Contents
* [Tutorial Sites](#Tutorial Sites)
* [Lookup Tables](#lookup-tables)
* [Mathematics And Stuff](#mathematics-and-stuff)
* [Programming Guides](#programming-guides)
  * [General](#general)
  * [Components](#components)
  * [AI](#ai)
  * [XNA](#xna)
  * [Graphics / Effects](#graphics-/-effects)
  * [HLSL Shaders](#hlsl-shaders)
  * [Audio](#audio)
* [Tools](#tools)
* [Artistic Material](#artistic-material)
  * [Graphics](#graphics)
  * [Fonts](#fonts)
  * [Sounds](#sounds)

## Tutorial Sites 
No specific order.  
* [**Shawn Hargreave's Blog**](http://blogs.msdn.com/b/shawnhar/) - This is a must-read for every XNA developer. The blog of the Master himself.
* [**XNAdevelopment**](http://www.xnadevelopment.com/tutorials.shtml) - Great beginners tutorials around XNA game development.
* [**Catalin Zima's Blog**](http://www.catalinzima.com) - You should all know this one (and you will, I promise). Good examples. I would say that most of the content in here is for the advanced beginner.
* [**Riemer's XNA Tutorials**](http://www.riemers.net/) - Flood of useful tutorials. I found it a bit untidy in a way.
* [**digitalerr0r**](http://digitalerr0r.wordpress.com/tutorials/) - HLSL tutorials for every level of expertise. Nice guy but sort of retired, sadly.
* [**Kyle Schouviller's Blog**](http://www.kyleschouviller.com/) - Good tutorials. Focus on content and tooling.
* [**RB Whitaker's Wiki**](http://rbwhitaker.wikidot.com/xna-tutorials) - Extremely versatile. Covers almost every aspect of XNA game development. Many thanks.
* [**Threading in C#**](http://www.albahari.com/threading/) - A must-read for every programmer.
* [**XNA Game Tutorials**](http://xnatd.blogspot.co.at/) - Some XNA game tutorials (2D collision, etc…)
   
## Lookup Tables 
This section contains tables that I found useful during game-development.  
* [**Color Charts**](http://www.kyleschouviller.com/xna/xna-color-charts/) - You want to set a color, but you can't see it?  
This site has proved most useful for me. There is not a single day that I don't visit it. It contains all the named colors you may use directly in XNA (or windows respectively), sorted the way you want.  
He has some more stuff going on at his blog, but frankly I didn't have the time to look into it.  
   
## Mathematics And Stuff 
This section contains articles about mathematical problems. You can't do without.
* [**Trajectory Calculations**](http://stackoverflow.com/questions/966935/trajectory-math-c-sharp) - Want your bullet to fly the right way?  
These links show you how to do the necessary math for a 3D trajectory.
* [**Curve-Path**](http://stackoverflow.com/questions/3273396/animate-sprite-along-a-curve-path-in-xna)
* [**Ballistic Trajectory**](http://www.gamedev.net/topic/333044-does-anybody-have-a-simple-ballistic-trajectory-algorithm-i-can-use/)
* [**Calculate a bounce-angle**](http://stackoverflow.com/questions/573084/how-to-calculate-bounce-angle) - Want your ball to bounce off the wall?
This StackOverflow topic shows you how to do the necessary math.  
* [**Collision Detection Overview in XNA**](http://msdn.microsoft.com/en-us/library/bb313876%28v=xnagamestudio.20%29.aspx) - You want the monster to die, when you hit it?
This is a good and very general overview. It describes the procedure using XNA-datastructures (which isn't always the best choice), but I think that this is a "must read".  
* [**Line Intersection**](http://community.topcoder.com/tc?module=Static&d1=tutorials&d2=geometry2) - You have intersecting lines but you don't know the intersection point?
Helpful formulas when wanting to know the intersection-point of lines in general.  
* [**Intersection Tests**](http://www.gamasutra.com/view/feature/3383/simple_intersection_tests_for_games.php?page=1) - You want to know the point where the bullet hit the plane?
This is THE site containing an abundance of intersection tests for various geometric primitives. Must read. Thank you very much Miguel Gomez.  
* [**Separating Axis Theorem (SAT)**](http://www.metanetsoftware.com/technique/tutorialA.html) - You want to know, if the ray hit the polygon?  
By the way: AABB means Axis-Aligned-Bounding-Box.
This is a very interesting and helpful technique (and straight forward).  

## Programming Guides 
This section contains tips about how to structure your programs or how to achieve certain tasks necessary for game-deployment.

### General
* [**Shadow-Copying of Applications**](http://www.codeproject.com/Articles/29961/Shadow-Copying-of-Applications) - You want your installer to delete itself in windows?  
You might come to a point where you'll end up writing your setup or updating your application, where you want to unload a program, that is currently running. In general that's not easily possible, but this project might help. We circumvented the issue by using a WIX setup (you are able to run programs before and afterwards that are not present on the disk, but in the GAC, which is very nice; We deleted the install-directory that way by running a C# deletion-program leaving no trace of the game whatsoever).
* [**Repositioning The Cursor**](http://www.pinvoke.net/default.aspx/user32.setcursorpos) - You want to reposition or clamp the windows cursor to or within a window?  
On a multi-monitor setup you should prevent the mouse cursor from leaving the monitor your customer is playing on. Here you'll find the proper interop-calls (I'm sure you know this site).
* [**Saving The State of Your Game**](http://stackoverflow.com/questions/3723287/what-is-a-good-example-of-saving-game-data-in-xna-4-0) - You want to create a save-game? This is a very quick and elegant method to accomplish this by using XML.  
* [**Get Special Folders**](http://dn.embarcadero.com/article/32384) - You want to save your save-game in %appdata%?
* This page shows you how to get the paths of these special directories regardless of the version of windows your customer is running. Necessary to avoid "no write permission" errors on saving any game-data.  
* [**Multi CPU Usage**](http://www.codeproject.com/Articles/7933/Smart-Thread-Pool#Feature5) - You want to use all of the CPU cores on your customer's machine?  
You may want to use .NET's new parallels framework or, if you are stuck with an older .NET framework, write one of your own.
* [**'Non-Blocking' Synchronization**](http://www.albahari.com/threading/part4.aspx) - You want your code synchronized without blocking waits?  
This is the premier-league of multi-threaded-programming. It's very difficult and subtle. Fasten your seatbelts, you're in for some ride.
* [**Decompress DXT Textures**](http://www.gamedev.net/topic/467156-dxt-decompress-in-c/) - You want to manually decompress DXT Format Files?
* There are not many reasons for you to want to do this, but nevertheless. Here it is.  

### Components
This stuff here is ripped from our game. For you to take and use as you like.
* [**Object Pool**](https://gist.github.com/guFalcon/39a24c1c0bba644a2ba3e03f53601632) - This is a lock-free object pool. One of the integral parts of a game-engines.
* [**Collision Grid**](https://github.com/UnterrainerInformatik/collisiongrid) - Used in the broad-phase of collision detection. Faster than a Quad-Tree. Description is inside.
* [**SplitStopWatch**](https://github.com/UnterrainerInformatik/splitstopwatch) - Want to debug timings and you like a pretty console-output using split-times, etc? Take this.
* [**ThreadPool**](https://github.com/UnterrainerInformatik/threadpool) - Want to do async work but the methods you like to call all have different signatures? This is a very fast implementation of a fill-and-start thread pool.
* [**Per Pixel Collision**](https://github.com/UnterrainerInformatik/perPixelCollision) - Want to know how to do matrix-transformations? Want to know if two textures collide with pixel-precision? Take this, but read the readme.md first. It explains why using this technique in a production environment is a bad idea.

### AI
* [**Path-Finding**](http://www.codeproject.com/Articles/5758/Path-finding-in-C) - You want your hero to find the right way?
This is a good implementation of the A* Algorithm. You have to modify it of course, because the garbage collector would kill you in no time, but it's a good starting point.  

### XNA
* [**XNA 3.11 to XNA 4.0 Conversion Cheat Sheet**](http://nelxon.com/resources/xna-3-1-to-xna-4-0-cheatsheet.php) - You want to change XNA 3.1 code to 4.0?
This is a great help when searching for a way to get things done the right way. Many examples.  
* [**Getting A List Of Supported Display Modes**](http://blog.gallusgames.com/xna/getting-a-list-of-supported-display-modes-in-xna) - You want to know the resolutions your client's machine supports
This one is very simple. You just ask XNA and you'll get what you want.  
* [**2D Camera With Zoom And Rotation**](http://www.david-amador.com/2009/10/xna-camera-2d-with-zoom-and-rotation/) - You want to write a platformer?
This is a tutorial on how to implement a proper camera for a 2D game.  

### Graphics / Effects
* [**Using Shaders**](http://www.xnamag.de/article.php?aid=34) - You want to use shaders and don't know what that is?
Then this site is a good place to start.  
* [**3D Model Drawing Guide**](http://www.3dgameprogramming.net/2007/06/04/getting-started-with-xna-drawing-a-3d-model/) - You want to draw a 3D model in XNA?
This guide shows, step by step, how to draw a mesh in XNA. Nicely done, thank you very much.  
* [**2D Circles And Lines**](http://xboxforums.create.msdn.com/forums/p/7414/200025.aspx) - Want to draw 2D using XNA?Well. Then you're in for a treat!  
It's impossible to do that without completely destroying the performance of your game. But since you're inevitably sitting on a high-performance-graphics-workhorse already, you may draw 3D as well. These links show you how.
* [**2D Circles And Lines**](http://www.bit-101.com/blog/?p=2832)
* [**Premultiplied Alpha And Alpha-Blending**](http://blogs.msdn.com/b/shawnhar/archive/2009/11/06/premultiplied-alpha.aspx) - You want to understand the intricacies of this subject?
Well. Here is the Master of XNA for you. May I present: Shawn Hargreaves...  
* [**Post Processing Effects**](http://www.float4x4.net/index.php/2011/02/xna-after-effects-part-1/) - You want a bloom-filter?
This tutorial explains the usage and limitations of such an effect.  
* [**Dynamic 2D Shadows**](http://www.catalinzima.com/samples/12-months-12-samples-2008/dynamic-2d-shadows/) - You want a flashlight in your 2D game?
This is one of the most popular tutorial-sites out there. I cannot thank Catalin enough for his efforts making this site.  

### HLSL Shaders
* [**Graphics Pipeline Diagram**](http://www.riemers.net/eng/Tutorials/XNA/Csharp/Series3/HLSL_introduction.php) - You are stuck programming your shader and don't know what happens and when?
This is a very popular site about XNA game development in general. This particular page contains a very useful diagram of the graphics rendering pipeline, that may lighten things up a bit during dark, non-comprehending times (you will have that, I promise).  
* [**HLSL Language Reference**](http://msdn.microsoft.com/en-us/library/windows/desktop/ff471376(v=vs.85).aspx) - Want to know how HLSL works?
This is Microsoft's HLSL reference. Nothing more, nothing less.  
* [**Wiggle Effect**](http://digitalerr0r.wordpress.com/2009/04/22/xna-shader-programming-tutorial-9-post-process-wiggle/) - Want your background to wiggle?
Then this tutorial is for you. Presented to you by digitalerr0r, a great site for HLSL tutorials.  
* [**Bloom Post Process Filter**](http://digitalerr0r.wordpress.com/2009/10/04/xna-shader-programming-tutorial-24-bloom/) - Want your game to shine?
This tutorial explains the use of post process filters and the bloom filter. Many pictures. Expertly commented. Recommended.  
* [**GPU Driven Terrain Mapping**](http://allenwp.com/blog/2010/05/06/simple-fast-gpu-driven-multi-textured-terrain/) - You want to render your terrain given a low-res terrain-map-texture?  
This example uses a low-res terrain-map-texture (where the information which tile to draw is encoded in the colors) to render a terrain. Advanced and only usable under certain circumstances, but worth the time.  

### Audio
* [**XACT Audio Tutorials**](http://rbwhitaker.wikidot.com/audio-tutorials) - You want to make noise, but you don't know how?
This is a very elaborate collection of very useful tutorials starting from "Audio in XNA" and ending with "3D Audio Effects". Very straight forward and many screenshots.  
* [**Attenuation / Doppler Pitch Shifting in XACT**](http://msdn.microsoft.com/en-us/library/dd231913.aspx) - You want your close sprites to be louder than the ones far away?  
Very elaborate Microsoft tutorial on creating attenuation and doppler-pitch-shifting using XACT. Nice, step by step and many screenshots.  

## Tools
* [**wyBuild**](http://wyday.com/wybuild/features.php) - You want to have an updating game (maybe self-updating)?
A tool to create and deliver AND install updates manually or automatically in any given .NET language. This one saved and saves our butts during the alpha-testing stage.  
* [**Convert to Icon**](http://converticon.com/) - You want your own mouse-cursor?
When programming a game in XNA you come to a point when you want your own mouse-cursor. This program helps you to convert your image-files to an icon-file. And it's completely online.  
* [**DXT Compression**](http://code.google.com/p/libsquish/) - You want to compress the textures of your game on your own?
Normally you'd use the content-loader-pipeline of XNA (don't fear; the content-loader-pipeline does almost everything automatically), but if you can't use it, then you'll be stuck with this when you're trying to get compressed textures to your graphics-card.  

## Artistic Material 
All the sites I link to in this paragraph contain "free for commercial use" material, although they may contain non-free material as well. It's your responsibility to check before you use it.  
You won't be able to dodge the fight with the even or odd license when dealing with creative content, so you might as well get over it.  

### Graphics
You want a sky-, grass- or other texture?  
These sites contain, besides other stuff, free-for-commercial-use textures.  
* http://www.noctua-graphics.de/deutsch/fraset_d.htm  
* http://telias.free.fr/  
* http://www.cgtextures.com/  

### Fonts
You want to write something on the screen without getting sued?  
These sites contain, besides other stuff, many free-for-commercial-use fonts (you'll have to read the licenses though).  
* http://www.fontsquirrel.com

### Sounds
You've got no sound yet?These sites contain, besides other stuff, free-for-commercial-use samples.  
* http://www.mediacollege.com/downloads/sound-effects/
* http://www.partnersinrhyme.com/pirsounds/WEB_DESIGN_SOUNDS_WAV/BUTTONS.shtml
