# GitHub Pages Setup Guide for TradeBlocker Updates

This guide will help you set up GitHub Pages to host your Sparkle updates.

## 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com/) and sign in to your account
2. Click on the "+" button in the top-right corner and select "New repository"
3. Name the repository `TradeBlocker-updates`
4. Add a description (optional)
5. Make the repository public
6. Initialize with a README (optional)
7. Click "Create repository"

## 2. Upload Your Update Files

1. Clone the repository to your local machine:
   ```
   git clone https://github.com/YOUR_USERNAME/TradeBlocker-updates.git
   ```

2. Copy the contents of this directory (TradeBlocker-updates) to the cloned repository:
   ```
   cp -R TradeBlocker-updates/* path/to/cloned/repo/
   ```

3. Add, commit, and push your files:
   ```
   cd path/to/cloned/repo
   git add .
   git commit -m "Initial commit with Sparkle update structure"
   git push
   ```

## 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings"
3. Scroll down to the "GitHub Pages" section
4. Under "Source", select "main" branch
5. Click "Save"
6. Your site will be published at `https://ALBI0NE.github.io/TradeBlocker-updates/`

## 4. Update Your App's Info.plist

1. Update the `SUFeedURL` key in your app's Info.plist to point to your GitHub Pages URL:
   ```xml
   <key>SUFeedURL</key>
   <string>https://ALBI0NE.github.io/TradeBlocker-updates/appcast.xml</string>
   ```

## 5. Creating and Publishing Updates

1. Build your app in Xcode
2. Run the create-dmg.sh script to generate a DMG file
3. Sign the DMG with your Sparkle private key
4. Update the appcast.xml file with the new version information and signature
5. Commit and push the changes to GitHub
6. Create a GitHub Release with the DMG file as an attachment

## 6. Testing Updates

1. Install an older version of your app
2. Run the app and trigger the update check
3. The app should detect the new version and prompt for an update 