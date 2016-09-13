# GameDevelopmentLinks
This is a collection of useful game-development links including, but not restricted to, development with MonoGame.
https://gist.github.com/guFalcon/39a24c1c0bba644a2ba3e03f53601632

During the process of developing our game I came across a large variety of websites that I found very useful.  
This page is a collection of all of them baring a short description. I will check in every month or so and update this list accordingly.  
Let me mention that I didn't record those links in any particular order and that the sites, I link to in this section, may contain much more than the description of the link suggests. Chances are that I didn't even look through each and every page of every single site before finding it helpful and bookmarking it. These are just the pages I found searching for solutions for the problems in the various fields of interest you inevitably stumble over when starting to write a game.  
  
I tried to sort every link-table it in a way that should benefit your learning curve (most complex subjects last).  

If you want to contribute just fork this repo, make changes and then a pull request.
Contributions are welcome!

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

### Trajectory Calculations
Want your bullet to fly the right way?  
These links show you how to do the necessary math for a 3D trajectory.  

* [**Trajectory-Math**](http://stackoverflow.com/questions/966935/trajectory-math-c-sharp) - A StackOverflow article with some helpful formulas.

#### Ballistic
* [**Curve-Path**](http://stackoverflow.com/questions/3273396/animate-sprite-along-a-curve-path-in-xna)
* [**Ballistic Trajectory**](http://www.gamedev.net/topic/333044-does-anybody-have-a-simple-ballistic-trajectory-algorithm-i-can-use/)  
#### Bounce Angle
Want your ball to bounce off the wall?

* [**Calculate a bounce-angle**](http://stackoverflow.com/questions/573084/how-to-calculate-bounce-angle) - This StackOverflow topic shows you how to do the necessary math.  
   
#### Collision Detection Overview in XNA
You want the monster to die, when you hit it?  

* [**XNA Collisions (MSDN)**](http://msdn.microsoft.com/en-us/library/bb313876%28v=xnagamestudio.20%29.aspx) - This is a good and very general overview. It describes the procedure using XNA-datastructures (which isn't always the best choice), but I think that this is a "must read".  

#### Line Intersection
You have intersecting lines but you don't know the intersection point?  

* [**TopCoder**](http://community.topcoder.com/tc?module=Static&d1=tutorials&d2=geometry2) - Helpful formulas when wanting to know the intersection-point of lines in general.  
   
#### Intersection Tests
You want to know the point where the bullet hit the plane?  

* [**Gamasutra - Intersection Tests**](http://www.gamasutra.com/view/feature/3383/simple_intersection_tests_for_games.php?page=1) - This is THE site containing an abundance of intersection tests for various geometric primitives. Must read. Thank you very much Miguel Gomez.  

#### Separating Axis Theorem
You want to know, if the ray hit the polygon?  
By the way: AABB means Axis-Aligned-Bounding-Box.  

* [**MetaNetSoftware - SAT**](http://www.metanetsoftware.com/technique/tutorialA.html) - This is a very interesting and helpful technique (and straight forward).  

## Programming Guides 
### General
   
#### Shadow-Copying of Applications
You want your installer to delete itself in windows?  
You might come to a point where you'll end up writing your setup or updating your application, where you want to unload a program, that is currently running. In general that's not easily possible, but this project might help. We circumvented the issue by using a WIX setup (you are able to run programs before and afterwards that are not present on the disk, but in the GAC, which is very nice; We deleted the install-directory that way by running a C# deletion-program leaving no trace of the game whatsoever).  

* [**CodeProject - Shadow-Copying**](http://www.codeproject.com/Articles/29961/Shadow-Copying-of-Applications)

#### Repositioning The Cursor
You want to reposition or clamp the windows cursor to or within a window?  
On a multi-monitor setup you should prevent the mouse cursor from leaving the monitor your customer is playing on. Here you'll find the proper interop-calls (I'm sure you know this site).  

* [**PInvoke.net**](http://www.pinvoke.net/default.aspx/user32.setcursorpos)

#### Saving The State of Your Game
You want to create a save-game?  

* [**Saving Game Data**](http://stackoverflow.com/questions/3723287/what-is-a-good-example-of-saving-game-data-in-xna-4-0) - This is a very quick and elegant method to accomplish this by using XML.  

###### Get Special Folders
You want to save your save-game in %appdata%?  
This page shows you how to get the paths of these special directories regardless of the version of windows your customer is running. Necessary to avoid "no write permission" errors on saving any game-data.  
http://dn.embarcadero.com/article/32384  
   
###### Multi CPU Usage
You want to use all of the CPU cores on your customer's machine?  
You may want to use .NET's new parallels framework or, if you are stuck with an older .NET framework, write one of your own.   This is a very cool article.  
http://www.codeproject.com/Articles/7933/Smart-Thread-Pool#Feature5  
   
###### Non-Blocking Synchronization
You want your code synchronized without blocking waits?  
This is the premier-league of multi-threaded-programming. It's very difficult and subtle.  
http://www.albahari.com/threading/part4.aspx  
   
###### Decompress DXT Textures
You want to manually decompress DXT Format Files?  
There are not many reasons for you to want to do this, but nevertheless. Here it is.  
http://www.gamedev.net/topic/467156-dxt-decompress-in-c/  
   
   
##### AI
###### Path-Finding
You want your hero to find the right way?  
This is a good implementation of the A* Algorithm. You have to modify it of course, because the garbage collector would kill you in no time, but it's a good starting point.  
http://www.codeproject.com/Articles/5758/Path-finding-in-C  
   
   
##### XNA
   
###### XNA 3.11 to XNA 4.0 Conversion Cheat Sheet
You want to change XNA 3.1 code to 4.0?  
This is a great help when searching for a way to get things done the right way. Many examples.  
http://nelxon.com/resources/xna-3-1-to-xna-4-0-cheatsheet.php  
   
###### Getting A List Of Supported Display Modes
You want to know the resolutions your client's machine supports?  
This one is very simple. You just ask XNA and you'll get what you want.  
http://blog.gallusgames.com/xna/getting-a-list-of-supported-display-modes-in-xna  
   
###### 2D Camera With Zoom And Rotation
You want to write a platformer?  
This is a tutorial on how to implement a proper camera for a 2D game.  
http://www.david-amador.com/2009/10/xna-camera-2d-with-zoom-and-rotation/  
   
   
##### Graphics / Effects
   
###### Using Shaders
You want to use shaders and don't know what that is?  
Then this site is a good place to start.  
http://www.xnamag.de/article.php?aid=34  
   
###### 3D Model Drawing Guide
You want to draw a 3D model in XNA?  
This guide shows, step by step, how to draw a mesh in XNA. Nicely done, thank you very much.  
http://www.3dgameprogramming.net/2007/06/04/getting-started-with-xna-drawing-a-3d-model/  
   
###### 2D Circles And Lines
Want to draw 2D using XNA?Well. Then you're in for a treat!  
It's impossible to do that without completely destroying the performance of your game. But since you're inevitably sitting on a high-performance-graphics-workhorse already, you may draw 3D as well. These links show you how.  
http://xboxforums.create.msdn.com/forums/p/7414/200025.aspx  
http://www.bit-101.com/blog/?p=2832  
   
###### Premultiplied Alpha And Alpha-Blending
You want to understand the intricacies of this subject?  
Well. Here is the Master of XNA for you. May I present: Shawn Hargreaves...  
http://blogs.msdn.com/b/shawnhar/archive/2009/11/06/premultiplied-alpha.aspx  
   
###### Post Processing Effects
You want a bloom-filter?
This tutorial explains the usage and limitations of such an effect.  
http://www.float4x4.net/index.php/2011/02/xna-after-effects-part-1/  
   
###### Dynamic 2D Shadows
You want a flashlight in your 2D game?  
This is one of the most popular tutorial-sites out there. I cannot thank Catalin enough for his efforts making this site.  
http://www.catalinzima.com/samples/12-months-12-samples-2008/dynamic-2d-shadows/  
   
   
##### HLSL Shaders
   
###### Graphics Pipeline Diagram
You are stuck programming your shader and don't know what happens and when?  
This is a very popular site about XNA game development in general. This particular page contains a very useful diagram of the graphics rendering pipeline, that may lighten things up a bit during dark, non-comprehending times (you will have that, I promise).  
http://www.riemers.net/eng/Tutorials/XNA/Csharp/Series3/HLSL_introduction.php  
   
###### HLSL Language Reference
Want to know how HLSL works?This is Microsoft's HLSL reference. Nothing more, nothing less.  
http://msdn.microsoft.com/en-us/library/windows/desktop/ff471376(v=vs.85).aspx  
   
###### Wiggle Effect
Want your background to wiggle?  
Then this tutorial is for you. Presented to you by digitalerr0r, a great site for HLSL tutorials.  
http://digitalerr0r.wordpress.com/2009/04/22/xna-shader-programming-tutorial-9-post-process-wiggle/  
   
###### Bloom Post Process Filter
Want your game to shine?  
This tutorial explains the use of post process filters and the bloom filter. Many pictures. Expertly commented. Recommended.  
http://digitalerr0r.wordpress.com/2009/10/04/xna-shader-programming-tutorial-24-bloom/  
   
###### GPU Driven Terrain Mapping
You want to render your terrain given a low-res terrain-map-texture?  
This example uses a low-res terrain-map-texture (where the information which tile to draw is encoded in the colors) to render a terrain. Advanced and only usable under certain circumstances, but worth the time.  
http://allenwp.com/blog/2010/05/06/simple-fast-gpu-driven-multi-textured-terrain/  
   
   
##### Audio
   
###### XACT Audio Tutorials
You want to make noise, but you don't know how?  
This is a very elaborate collection of very useful tutorials starting from "Audio in XNA" and ending with "3D Audio Effects". Very straight forward and many screenshots.  
http://rbwhitaker.wikidot.com/audio-tutorials  
   
###### Attenuation / Doppler Pitch Shifting in XACT
You want your close sprites to be louder than the ones far away?  
Very elaborate Microsoft tutorial on creating attenuation and doppler-pitch-shifting using XACT. Nice, step by step and many screenshots.  
http://msdn.microsoft.com/en-us/library/dd231913.aspx  
   
   
##### Tools
   
###### wyBuild
You want to have an updating game (maybe self-updating)?  
A tool to create and deliver AND install updates manually or automatically in any given .NET language. This one saved and saves our butts during the alpha-testing stage.  
http://wyday.com/wybuild/features.php  
   
###### Convert to Icon
You want your own mouse-cursor?  
When programming a game in XNA you come to a point when you want your own mouse-cursor. This program helps you to convert your image-files to an icon-file. And it's completely online.  
http://converticon.com/  
   
###### DXT Compression
You want to compress the textures of your game on your own?  
Normally you'd use the content-loader-pipeline of XNA (don't fear; the content-loader-pipeline does almost everything automatically), but if you can't use it, then you'll be stuck with this when you're trying to get compressed textures to your graphics-card.  
http://code.google.com/p/libsquish/  
   
   
#### Artistic Material 
All the sites I link to in this paragraph contain "free for commercial use" material, although they may contain non-free material as well. It's your responsibility to check before you use it.  
You won't be able to dodge the fight with the even or odd license when dealing with creative content, so you might as well get over it.  
   
##### Graphics
You want a sky-, grass- or other texture?  
These sites contain, besides other stuff, free-for-commercial-use textures.  
http://www.noctua-graphics.de/deutsch/fraset_d.htm  
http://telias.free.fr/  
http://www.cgtextures.com/  
   
   
##### Fonts
You want to write something on the screen without getting sued?  
These sites contain, besides other stuff, many free-for-commercial-use fonts (you'll have to read the licenses though).  
http://www.fontsquirrel.com  
   
   
##### Sounds
You've got no sound yet?These sites contain, besides other stuff, free-for-commercial-use samples.  
http://www.mediacollege.com/downloads/sound-effects/  
http://www.partnersinrhyme.com/pirsounds/WEB_DESIGN_SOUNDS_WAV/BUTTONS.shtml  
