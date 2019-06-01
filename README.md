# RNfbsdk

## Template and Instructions to add FBsdk login button to React Native Projects

### Steps
* based off of here -> https://developers.facebook.com/docs/react-native
1. react-native init [YOUR-PROJECT-HERE]
2. cd [YOUR-PROJECT-HERE]
3. react-native install react-native-fbsdk
4. react-native link react-native-fbsdk

#### Configuring for ios
5. cd ios
6. open [YOUR-PROJECT-HERE]
7. open [YOUR-PROJECT-HERE].xcodeproj
8. Click on top level project in XCode and find your **bundle identifier**
9. Go to this website - https://developers.facebook.com/docs/react-native
10. Register your app and then come back to this page and select from the drop down
11. Download FBsdk and save in your Documents folder
12. ONLY DO THE FOLLOWING STEPS - 
  * Click on bundle identifier and paste identifier
  * Replace `AppDelegate.m` with the contents of this repo's `AppDelegate.m` file
13. Execute the following command in your project root (not the ios folder, but your project root)
* `curl -O https://raw.githubusercontent.com/facebook/react-native-fbsdk/master/bin/ios_setup.js`
14. Run this command next
* `npm install plist xcode adm-zip`
15. Visit this site to obtain your app id
* https://developers.facebook.com/apps/
16. Run this command (no square brackets):
* `node ios_setup.js [App ID] [YOUR-PROJECT-HERE]`
17. Look at `components/LoginButton.js` to see Login button implementation and `App.js` for import and use
