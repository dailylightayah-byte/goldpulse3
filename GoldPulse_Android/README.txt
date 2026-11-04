GOLDPULSE ANDROID — BUILD AND INSTALL

This project wraps the GoldPulse web application in Capacitor Android and uses GitHub Actions to build an installable APK.

REPOSITORY UPLOAD
1. Open your GitHub repository: https://github.com/dailylightayah-byte/goldpulse
2. Upload the CONTENTS of this folder to the repository root (not the outer GoldPulse_Android folder).
   The repository root should contain:
   - www/index.html
   - package.json
   - capacitor.config.json
   - .github/workflows/build-apk.yml
   - .gitignore
   - README.txt
3. Commit to the main branch. GitHub Actions should automatically start the "Build Android APK" workflow.
4. If it does not start, open Actions, enable workflows if GitHub asks, then run "Build Android APK" using Run workflow.
5. When it completes successfully, open the run and download the "GoldPulse-APK" artifact. GitHub downloads the artifact as a ZIP; extract app-debug.apk.
6. Send app-debug.apk to the Android phone. Open it and permit installation from that source if Android prompts.

ANDROID APP
- App ID: com.goldpulse.journal
- App name: GoldPulse
- Offline-capable app content is bundled locally.
- Local app data is stored on the phone. Export a JSON backup and keep it safe before uninstalling or switching phones.
- To move existing journal data from the laptop app, use its "Download backup JSON" feature, then import that JSON in the phone app.
- Exported data is not automatically synchronized between devices.

BUILD NOTES
- The workflow builds a debug APK. It is suitable for personal installation, not Play Store publication.
- APK artifacts expire after 30 days on GitHub; download and save your APK locally/Drive. The installed app itself does not expire.
- Keep a backup of your data. Uninstalling the app may erase app-local data.
