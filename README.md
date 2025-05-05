# TradeBlocker Updates

This repository hosts updates for the TradeBlocker macOS application.

## Structure

- `appcast.xml`: The Sparkle appcast file that contains information about available updates
- `releases/`: Directory containing release artifacts (DMG files)

## Adding New Releases

1. Build the macOS app
2. Create a DMG installer
3. Sign the DMG with the Sparkle private key
4. Update the appcast.xml with the new version information
5. Commit and push changes
6. Create a new GitHub release with the DMG as an asset

## Using Sparkle for Updates

TradeBlocker uses [Sparkle](https://sparkle-project.org/) for automatic updates. The application will check for updates automatically and prompt the user when a new version is available.

Users can also manually check for updates from the application menu: TradeBlocker > Check for Updates. 