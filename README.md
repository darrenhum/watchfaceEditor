# watchfaceEditor
Bip watchface viewer and editor


This tutorial does not require the use of either Tasker or Tools & Amazfit and thus can be done for free.
1. In order to start to create a custom watch face, first you need a watch face template.
2. Connect your BIP to your android phone via MiFit app.
3. Open MiFit, goto Profile->Amazfit Bip->Watch face settings
4. Click on the ugliest watch face (in your opinion, i used the 'Number'' watch face and press 'Sync watch face'
5. Watch face should be synced to your BIP and downloaded to your phone.
6. Connect your Android phone to your PC and navigate to 'Android/data/com.xiaomi.hm.health/files/watch_skin' and transfer the .bin file to your working directory on your PC. 
(For my case, the .bin file is named '9098940e097cf25a971fc917630a6ac2.bin'. That is the name of the 'Number' watch face. Your .bin file may have a different name and that is ok)
7. Download Amazfit Tools to your PC from this link: https://bitbucket.org/valeronm/amazf...ols/downloads/
8. Extract the downloaded file to a folder and then drag and drop the transferred .bin file on 'WatchFace.exe' A cmd window should appear and disappear in a flash.
9. A folder with the name of your .bin file should now appear in folder where your .bin file is stored. (In my case, the folder is named '9098940e097cf25a971fc917630a6ac2')
10. Open the folder that appeared and inside you can see the components of a BIP watch face

11. In the folder, have 2 main file types, .png and .json (Delete the .log file and the 2 preview files)
12. The .png files are resources for the watch face (such as backgrounds, numbers etc) while the .json file contains code for the picture placements and watch face functions.
13. Now, you can either make small edits to the preexisting .png files with a photo editor (paint/gimp/photoshop) and then recompile to a .bin file
or
14. You can replace all the .png files with your own images 
(I will be going through this option more, people choosing the small edits path, after editing the resources, you can skip to recompiling the .bin, which is step 28)
15. If you choose to replace all the .png files with your own images, start creating your .png files now. Below are the requirements for the .png files
The screen size of the BIP is 176x176px, so do size your images accordingly
Must have at least 11 images, with 000.png being the background and 001.png being number 0, 002.png being number 1, so on till 010.png being number 9.
If you want to have a separate of images for minutes and hours it is possible. Your next set of images should start with 011.png being number 0.
16. Follow all the requirements and your folder will end up looking like this:

17. It is possible to edit the .json by hand but it is easier to do so with a GUI tool.
18. Go to https://v1ack.github.io/watchfaceEditor/ and upload all your custom images and the .json file respectively.
19. You may get a few error messages but just ignore them.
20. Go to the edit tab and replace the contents inside with this:

21. This is the most basic .json watch face code, giving you only the time in hours and minutes. The code explanation is below:

22. In the edit tab, there are a few options for you to play around in the sidebar. Do experiment and play around!
22. You can go to the design tab and start moving the numbers according to your own needs. 
23. There are many more watch face functions supported by the BIP and I recommend visiting this site. (Google translated) to learn more about them. The site is an amazing site with numerous watch face related tutorials but it is all in Spanish 
24. When satisfied with your watch face, press export JSON and download the .json file to your decompiled .bin file folder. Replace the existing .json file. (For me, the folder is the '9098940e097cf25a971fc917630a6ac2' folder)
25. Download this zip file: https://github.com/v1ack/watchfaceEd...aultimages.zip
26. Extract all the files in the downloaded file into your decompiled .bin file folder. These images are the ones used by the online watch face editor when you add functions such as date display, weather, steps etc etc
27. Your decompiled .bin folder should look like this now:

28. Drag and drop the .json file onto 'WatchFace.exe', '9098940e097cf25a971fc917630a6ac2_packed.bin' should appear in the folder (your file name should be different) alongside a few previews of your watch face.
29. Rename your packed .bin file by removing the '_packed.bin'. (In my case, my file is renamed from 9098940e097cf25a971fc917630a6ac2_packed.bin to 9098940e097cf25a971fc917630a6ac2.bin )
30. Transfer the newly created .bin file to your Android phone, into this folder: 'Android/data/com.xiaomi.hm.health/files/watch_skin' . Replace the old watch face .bin.
31. Open MiFit app and sync the watch face you synced at step 4 onto your BIP
32. Viola! You got a new custom watch face.
33. If you get any errors at step 28 (recompiling), check if you all all the images you referenced to in your .json in the folder. Also, go back to the watch editor website and check your .json file for any errors. You can comment below if you have anything that you are unsure of or need more clarifications.
