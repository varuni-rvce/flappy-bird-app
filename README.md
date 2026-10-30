# Flappy Bird (mobile app)

A Flappy Bird game built with plain HTML canvas and packaged as an Android and iOS app using [Capacitor](https://capacitorjs.com).

## Project layout

- `www/index.html`: the whole game (HTML, CSS, JS)
- `capacitor.config.json`: app id, name and web directory
- `package.json`: scripts and Capacitor dependencies

## Play in a browser

```bash
npm install
npm start
```

## Build the mobile apps

Before the first build, change `appId` in `capacitor.config.json` to your own reverse-domain id (for example `com.yourname.flappybird`).

```bash
npm install

# Android (needs Android Studio)
npm run add:android
npm run sync
npm run open:android     # press Run in Android Studio

# iOS (needs a Mac with Xcode)
npm run add:ios
npm run sync
npm run open:ios         # press Run in Xcode
```

After any change to `www/`, run `npm run sync` to copy it into the native projects.

## App icon and splash screen

Put `icon.png` (1024x1024) and `splash.png` (2732x2732) in an `assets/` folder, then run:

```bash
npx @capacitor/assets generate
```

## Controls

Tap, click, or press Space or the Up arrow to flap. Best score is saved on the device.
