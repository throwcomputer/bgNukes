bgNukes README

# Background
bgNukes is a tool for launching background renders from The Foundry's Nuke, a kick-ass compositing application. [http://www.thefoundry.co.uk/products/nuke/] It is written by Tim BOWMAN [http://netherlogic.com].

This script exists because our company renderfarm wasn�t alive yet and I was already frustrated with rendering in the Nuke UI and tired of typing out command-line render commands to background the renders. I am sharing it because I'm sure my situation was not unique.

Originally, I posted it as launchNukes_inNuke.py (I know -- awful name) on VFXTalk and on my blog [http://netherlogic.com]. As of now, the official home for bgRender will be on GitHub [http://github.com/timbowman/bgRender] and it will be found also on Nukepedia [http://www.nukepedia.com/].

# Details
This script launches a number of command-line render instances in the background and captures their output in log files which are saved to the same directory as the Nuke script. You are now free to keep working in the UI and have your renders happen in the background. You are also free to to launch 8 simultaneous command-line Nuke renderers and fully saturate your fancy 8-core MacPro.

It works in Nuke6.0 on OS X. One of my goals is to ensure that it also works on other versions and platforms. Maybe it already does. If you've tested it and it worked (or didn't) please let me know what happened.

# How to use it
Put bgNukes in your .nuke directory (or somewhere else in your Nuke path if you're fancy), then add this line to your menu.py:

import bgNukes

Importing the module adds a "BG Render" item to the Render menu. From here it's dead simple: load your Nuke script, select "BG Render", and tell it which frames and how many instances you want.

Happy Rendering!

# Thank you
Thanks go to Nathan Dunsworth. His localRender.py was (and continues to be) an excellent reference.

# LICENSE
Copyright (c) 2010 Tim BOWMAN

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.