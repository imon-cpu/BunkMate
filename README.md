# BunkMate Android project

This project packages the current BunkMate HTML app into an Android app using Capacitor. A GitHub Actions workflow is included to build a debug APK in the cloud, so you do not need to install Java or Android SDK tools locally.

## Build the APK online (cloud build)

1. Create a new repository on GitHub. A private repository is fine.
2. Upload the **contents** of this project folder to the repository, keeping the `.github/workflows/build-apk.yml` file in that exact path and keeping `www/index.html`.
3. In the repository, open **Actions** and select **Build BunkMate APK**.
4. Click **Run workflow** (or push/commit to the `main` branch to trigger it automatically).
5. When the run finishes successfully, open that run and download the **BunkMate-debug-APK** artifact.
6. Extract the downloaded artifact ZIP. It contains `app-debug.apk`. Transfer it to your Android phone and install it. Android may ask you to allow installs from the app you use to open the APK.

## Important

- This is a project that builds an APK, not a prebuilt APK.
- The workflow runs on GitHub's hosted runner. GitHub account limits and availability may apply.
- The current HTML app is bundled locally, so the app UI can open offline. Browser-based features and reminders may need extra native Android work to behave like full background notifications.
- The debug APK is for testing/personal installation, not Play Store publishing.
- Keep a backup of app data before replacing `www/index.html` with a newer version.
