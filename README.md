F_Record
A lightweight Photoshop plugin for recording the drawing process.
Plugin Principle: It uses Photoshop’s generator interface, capturing images whenever the canvas changes, and then strings them together to generate a video.
Supported Versions: Photoshop 2019 and later (Thanks to srylyx for compatibility support).
Supported Systems: Windows, Mac (The Mac version is simply replacing the relevant ffmpeg executables with the Mac version; everything else remains the same).
Github: https://github.com/F-know/F_Record (If you download from here, don’t download the entire repository’s source code; download the release instead).
Cloud Download: https://pan.quark.cn/s/d3aaf46abc5e
Disclaimer: This plugin doesn't guarantee flawless operation on every computer. For critical recording processes, make sure to have a Plan B. I am not responsible for any losses caused, as this plugin is free. If you still have questions after reading all of this, you can message me on Bilibili (ID: F_know) and I’ll reply when I see it.
PS Plugin Development Blog: https://uiscripting.com. I completed this plugin step by step by following the blog from this expert. It took me about a week.

Installation Instructions
If you’ve installed version 1.0 before, please delete it first. Don’t record part of a drawing process with two different versions.
If Photoshop doesn’t already have the following paths, you can create them yourself.

Windows
Place F_Record-CEP in /Adobe Photoshop/Required/CEP/extensions
Place F_Record-generator in /Adobe Photoshop/Plug-ins/Generator

Mac
Place F_Record-CEP in /Users/{username}/Library/Application Support/Adobe/CEP/extensions
Place F_Record-generator in /Adobe Photoshop/Plug-ins/Generator

Then open Photoshop, go to Edit > Preferences > Plug-ins, and check Enable Generator and Load Extension Panels. Restart Photoshop (be sure to restart!), and you’ll find the plugin under Window > Extensions.

If you’re using a Mac and the plugin doesn’t work properly, you can refer to the advice from a foreign user (I’m copying their original words since I’m not familiar with Mac):

I would suggest adding information into README about running the extension on ARM Mac hardware (M processors). To load plugins on the ARM version of Mac, it requires running Photoshop in "Rosetta" mode (check "open with Rosetta" in the "get info" file window of the Photoshop app icon).

Plugin Interface Parameters
Path: Enter the path where you want to save the process images and output video, not the plugin installation path. You can create a folder anywhere, then copy the path into the plugin.
Number of saved images: Shows the number of images saved during the process. This increases gradually as you work after starting the recording.
Minimum save interval: Controls the frequency of image saving. Usually, set this to 0. If the canvas is large (like over 5000x5000 pixels, depending on your computer’s performance), saving images may take longer, effectively increasing the minimum save interval.
Video duration: Controls the final video’s duration. You can fill this in after recording. I suggest keeping it under 5 minutes, as it correlates to the time spent generating the video (but if you don’t mind waiting longer, that’s fine too).

FAQs
Q: The plugin says it’s not properly signed?
A: Some file was modified or corrupted. Try redownloading. If that doesn’t work, search online for solutions—there are many available.

Q: Installed according to the tutorial, but the plugin doesn’t appear in the Extensions menu?
A: It’s most likely that the F_Record-CEP folder is in the wrong place.

Q: After clicking Start Recording, I get a “path not found” error?
A: Don’t include quotation marks in the path you enter.

Q: After starting the recording, the image count stays at zero?
A: Either the F_Record-generator folder is in the wrong place, or the canvas is too large, making saving very slow.

Q: Can I continue recording next time after closing Photoshop?
A: Yes, just click Continue Recording.

Q: What if I want to stop recording this drawing halfway and start a new one?
A: Create a new folder and use a new path. You can switch back later if you want.

Q: Will canvas cropping or expansion affect the video?
A: The video will automatically adjust.

Q: Will zooming, flipping, or rotating the canvas be recorded in the video?
A: If it only changes the canvas view and not the canvas itself, it won’t be recorded.

Q: Which canvas will be recorded if there are multiple open?
A: The one that’s selected when you click Start Recording.

Q: What affects the time it takes to output the video?
A: It mainly depends on the video duration you set, and somewhat on the number of images, but not on canvas size.

Q: Why is the video output stuck at 0%?
A: It’s likely because the video duration is set too long, or there are too few images. If you wait, it will eventually jump to 90%.

Q: I get an undefined error halfway through the video output?
A: Either you're using the first version with a large canvas (in which case you’ll have to use video editing software like Premiere to compile the images into a video), or there’s a corrupted image file (for example, if Photoshop was closed during the image saving process). Find and delete the corrupted image.

Unresolved Issues
Q: F_Record isn’t compatible with certain other plugins when used simultaneously?
A: I use very few other Photoshop plugins, so I’m not sure why this happens.

Q: The plugin flashed briefly and disappeared?
A: This issue seems to occur with some versions of Photoshop 2019. Users have reported that reinstalling Photoshop solves the problem.

Q: Will the plugin record hidden layers?
A: This rarely happens, but if it does, it could be due to a broken Photoshop generator. You can try reinstalling Photoshop.

Q: The video output has color discrepancies?
A: There is a slight difference, which was pointed out to me. I use ffmpeg to generate the video, and I suspect the issue comes from the color space conversion, but I haven’t figured out how to fix it yet.


