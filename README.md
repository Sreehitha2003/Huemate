# Huemate (Android app)

Point your camera at a shirt, kurta or saree. Huemate picks out its main
colours, names them the way you'd say them in a shop (mustard, rani pink,
mehendi green…), and suggests what goes with them using colour theory.
Save pieces to your wardrobe, see which of your clothes pair best, and check
any two colours together.

Works fully offline. No account, no API key, and your photos never leave the phone.

## Build the APK on GitHub (same as Idea Walk)
1. Create a new **private** repository, e.g. `huemate`.
2. Upload everything in this folder. On a Mac, press Cmd + Shift + . in Finder
   first so the hidden `.github` folder shows, then drag all the contents in.
   If the Actions tab stays empty, use Add file > Create new file, name it
   `.github/workflows/build-apk.yml`, and paste in that file's contents.
3. Actions tab > "Build Huemate APK" > wait about 4 minutes >
   download **Huemate-apk** and unzip it.
4. Put `Huemate.apk` in Google Drive, open it on your phone and install.

## Using it
- **Scan:** live colour under the ring. Tap the yellow button to capture, then
  tap anywhere on the photo to pick an exact spot. **Photo** opens your gallery.
- **Prints:** when a photo has several strong colours, the app treats it as a
  print and matches all its colours together (switch it off to match one colour).
- **Save** adds the piece to your closet. For prints, tick every colour it has.
- **Swipe:** pick a piece and swipe through outfit ideas: right to love,
  left to skip (or use the buttons). At the end, choose your final look
  from the ones you loved and save or share it.
- **Closet:** your pieces and saved looks. Tap a piece to see what it goes with.
- **Pair:** any two pieces or colours, scored out of 100 with the reason.

Tip: phone cameras shift colours under yellow indoor bulbs. Scan near a
window in daylight for the truest match.

## Files
- `app/src/main/assets/fonts/` – Gloock, Nothing You Could Do, Poppins and DM Mono, bundled so they work offline (all SIL Open Font License)
- `app/src/main/assets/index.html` – the whole UI and colour logic
- `app/src/main/java/.../MainActivity.java` – camera, photo picker, share sheet
- `app/palettematch.keystore` – signing key (password `palettematch-keystore`).
  Keep it: updates must be signed with the same key to install over the old version.
