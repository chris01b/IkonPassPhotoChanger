# IkonPassPhotoChanger
Change your Ikon Pass photo as many times as you'd like before it is printed.

## Requirements
1. Google Chrome
2. An Ikon Pass that has not been printed yet

## Tutorial
After some investigation, it is easier to change the code manually because Ikon uses Webpack's SplitChunksPlugin.
1. Navigate to [your Ikon account](https://account.ikonpass.com/myaccount).
2. Set up local overrides if it has not yet been configured. Take note of what folder overriden files are stored in. Do not edit any files.
3. Enable local overrides.
4. Press Command-Option-F to open the search tab of the console drawer. Enable regular expression searching by pressing the `.*` button. Search for `profilesNeedingPhoto:\w+\(\w+\)` and click the line of code in the results.
5. If not already enabled, enable pretty print with the `{ }` button at the bottom right of the code editor.
6. Hardcode your profile as needing a profile picture. Look for the `profilesNeedingPhoto` key on the screen. For example, if the value is already `Ad(e)`, replace its value with `[e.profile]`.
7. Press Command-S to save.
8. Refresh the Chrome tab.
9. At the top of the screen, you will see "YOUR MOUNTAIN CHECKLIST" and a hyperlink to the right of that with your first name where you can upload your new photo.
