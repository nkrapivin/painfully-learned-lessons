<h1 align="center">Painfully Learned Lessons</h1>

<p align="center"><i>A straight-forward guide to mitigate the various harms committed upon society by YoYoGames' masterwork of digital torture, <b>GameMaker</b>.</i></p>

<p align="center"><i>PRs welcome. Share your pain.</i></p>

&nbsp;

&nbsp;

### I am getting a shader compilation failure in GameMaker 2023 / 2022 / GameMaker Studio 2.
https://www.microsoft.com/en-us/download/details.aspx?id=30679

&nbsp;

### I am getting performance issues on Windows 11 and newer versions of Windows 10.
https://www.microsoft.com/en-us/download/details.aspx?id=30679

&nbsp;

### The game is crashing to desktop without an error message.

Try running the game in YYC to generate a C++ project, and then run the generated solution file through Visual Studio's debugger. This'll hopefully point you in the right direction. Even if you can't solve the problem, it'll make for a more informative bug report to YYG.

&nbsp;

### My `fps_real` is high but `fps` is low (performance is bad).
`fps_real` only measures what you're doing on the CPU. You're likely GPU-bound. Turn off graphical effects, reduce rendering resolution, draw less to the screen. Use RenderDoc to identify particular pain points.

&nbsp;

### `<insert library name here>` is taking up 50% of a Step in the profiler and I am very worried about it.
The GameMaker profiler is deceptive and the percentage measurement is nigh useless due to the way it's calculated. The bit that's actually important is the time taken to execute the function. If the execution time is less than 1ms then you're getting your knickers in a twist about nothing.

&nbsp;

### GameMaker is lagging whenever I add instances to a room.

Turn off Feather (at least for the duration that you're doing lots of heavy room editing).

&nbsp;

### What is GameMaker's GLSL ES version?
1.00 rev 17. Older versions of GameMaker have patchy support for standard derivatives, and no current (GMS2023.6 and before) versions of GameMaker natively support vertex texture fetching outside of HTML5.

&nbsp;

### My gamepad doesn't work.

Might be solved by using [Input](https://github.com/jujuadams/input).

&nbsp;

### I am getting a shader compilation failure in GameMaker Studio 1.
https://www.microsoft.com/en-gb/download/details.aspx?id=8109

&nbsp;

### I'm using GameMaker Studio 1 and my game has performance issues I can't figure out.

Try using [gmsched](https://github.com/skyfloogle/gmsched).
