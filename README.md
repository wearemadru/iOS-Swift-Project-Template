# iOS-Swift-Project-Template
# Step 1 - Rename the project

1. Click on the project you want to rename in the "Project navigator" on the left of the Xcode view.
2. On the right select the "File inspector" and the name of your project should be in there under "Identity and Type", change it to the new name.
3. Click "Rename" in a dropdown menu

# Step 2 - Rename the Scheme

1. In the top bar (near "Stop" button), there is a scheme for your OLD product, click on it, then go to "Manage schemes"
2. Click on the OLD name in the scheme, and it will become editable, change the name

# Step 3 - Rename the folder with your assets

1. Quit Xcode
2. In the correctly named master folder, there is a newly named xcodeproj file with the wrongly named OLD folder. Rename the OLD folder to your new name
3. Reopen the project, you will see a warning: "The folder OLD does not exist", dismiss the warning
4. In the "Project navigator" on the left, click the top level OLD folder name
5. In Utilities pane under "Identity and type" you will see the "Name" entry, change this from the OLD to the new name
6. Just below there is a "Location" entry. Click on a folder with the OLD name and chose the newly renamed folder

# Step 4 - Rename the Build plist data**

1. Click on the project in the "Project navigator" on the left, in the main panel select "Build Settings"
2. Search for "plist" in this section
3. Under packaging, you will see Info.plist, and Product bundle identifier
4. Rename the top entry in Info.plist
5. Do the same for Product Identifier

# Step 5 - Repeat step 3 for tests (if you have them)**
# Step 6 - Repeat step 3 for core data if it's name matches project name (if you have it)**

### Finally, you are done and can rebuild (Command + Shift + K to clean, Command + B to build)

# When using CocoaPods
# After step 2:

1. Quit XCode.
2. In the master folder, rename OLD.xcworkspace to NEW.xcworkspace.

# After step 4:

1. In XCode: choose and edit Podfile from the project navigator. You should see a target clause with the OLD name. Change it to NEW.
2. Quit XCode.
3. In the project folder, delete the OLD.podspec file.
4. rm -rf Pods/
5. Run pod install.
6. Open XCode.
7. Click on your project name in the project navigator.
8. In the main pane, switch to the Build Phases tab.
9. Under Link Binary With Libraries, look for libPods-OLD.a and delete it.
10. If you have an objective-c Bridging header go to Build settings and change the location of the header from OLD/OLD-Bridging-Header.h to NEW/NEW-Bridging-Header.h
11. Clean and run.
