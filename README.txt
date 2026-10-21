POCKET MAPPER - mobile app package

A) Fastest: install as an app (PWA, free, works offline)
1. Upload this whole folder to any free HTTPS host: Netlify Drop (app.netlify.com/drop), GitHub Pages or Cloudflare Pages.
2. Open the link on your phone.
   Android Chrome: menu > Install app
   iPhone Safari: Share > Add to Home Screen
3. It opens fullscreen like a normal app. File upload and camera work here.

B) Real APK / iOS app (Capacitor)
1. Install Node.js. In an empty folder run:
   npm init -y
   npm i @capacitor/core @capacitor/cli @capacitor/android @capacitor/ios
   npx cap init PocketMapper com.example.pocketmapper --web-dir=www
2. Make a folder "www" and copy index.html, manifest.webmanifest, sw.js and the icons into it.
3. npx cap add android   (and/or: npx cap add ios)
4. npx cap sync
5. npx cap open android  -> Android Studio -> Build > Build APK
   npx cap open ios      -> Xcode (needs a Mac)
Camera and microphone: add the usual permission entries in AndroidManifest.xml / Info.plist.
