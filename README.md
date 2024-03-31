# master-duel-mse
An MSE template containing a copy of DataEditorX and an MSE template for exporting Master Duel-style Images

# Extracting Card Images from YGO Omega

If you already have a list of card images (without borders) named by their card ID, you can skip to step 10 otherwise:

1. Download AssetStudio and YGO Omega if you haven't already, and open and update YGO Omega
2. Download this Git Repo Zip, and extract somewhere convenient.
3. Go to your YGO Omega install folder, and go to YGO Omega_Data/Files/Bundles and copy all of the "arts" folders somewhere else. You don't need any others.
4. run AssetStudioGUI.exe
5. in the AssetStudio Window, go to File > Load Folder
6. Load the folder containing all of the "arts" folders
7. Click the "Asset List" tab in AssetStudio, you should now see a large list of card images.
8. Go to Filter Type and select either "Sprite" or "Texture2D", doesn't matter which as every card image is duplicated as both a Sprite and a 2D Texture.
9. Afterwards to go Export > Filtered Assets and save all the images to a folder, and wait for the process to complete.
10. After this, copy all of the named images to your copy of this project's `data\yugioh-master-duel.mse-style\imagecode` (if an imagecode folder does not exist, create one.)

These will be your card images that you will load up.

# Exporting a Card Database as Card Pics

This list of instructions will assume you have a .cdb of cards you want to convert into images, if you have EDOPRO you'll likely have them in the "expansions" folder.

1. Download this Repository
2. Go to the "install these fonts" folder and install all the fonts you see inside this folder, as they are required for Magic Set Editor to render the text.
3. After having downloaded this repository and extracted it, you'll want to go to DataEditorX and run DataEditorX.exe
4. in DataEditorX, File > Open, and select your desired cdb, you should see a list of cards now.
5. in DataEditorX, go to MSE(M) > Save All As MSE-set
6. Name your MSE-set and save it somewhere, you may notice that your save will have created multiple files, this is normal for particularly large CDBs, it just means it split up your CDB into multiple 3000 card sets.
7. Open mse.exe, click "Open Existing Set" and select one of the sets you've saved
8. Provided you have the correct images, the card image should load automatically
9. IMPORTANT FOR PENDULUMS - Go to Set Info, and find the setting in MSE called "Pendulum image is small", click it and click "No", this will stop large Pendulum images from appearing squished. You will need to do this for each set.
10. Then hit File > Export > All Card Images, this should open a setting window.
11. Inside the "Format" section, paste this: `{to_string(to_int(card.gamecode))}.png`, if extracting to MDPro2, change out ".png" to ".jpg"
12. Make sure "Entire Set" is select and hit OK, and find an empty folder to save to.
13. Your images will now begin saving This process will take a while per set, and the Program may appear to hang, this is normal, if you want to see the progress of your images saving, go to the folder you've saved to in order to see progress.
14. After its done, wipe all images inside the "pics" folder of your EDOPRO, or the "picture/card" folder inside of MDPro2

# Some of my Pendulum cards look weird.

This is due to the fact that not all Pendulum Arts are made equal, I have provided a special MSE-set for this when extracting from Omega

1. open mse.exe as normal, but this time open the mse-set included in `included-sets`
2. This contains a list of Pendulums with small arts, simply Export all the Card Images with the instructions above to your card image folder and overwrite any duplicates.
