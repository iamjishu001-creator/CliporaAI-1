# Build Clipora AI APK using only an Android phone

1. Download and extract `CliporaAI-Android-Source.zip` on your phone.
2. In a browser, open https://github.com and sign in or create an account.
3. Create a new repository named `CliporaAI`. For the simplest setup, choose Public (do not upload API keys or secrets).
4. Open the repository, choose **Add file → Upload files**. Upload the *contents* of the extracted `CliporaAI` folder, including the hidden `.github/workflows/build-apk.yml` file. If the mobile file picker cannot show `.github`, create the workflow manually at `.github/workflows/build-apk.yml` using **Add file → Create new file** and paste the workflow contents from this guide's companion file `build-apk.yml`.
5. Commit the uploaded files to the `main` branch.
6. Open the repository's **Actions** tab. Select **Build Clipora AI APK** and tap **Run workflow** if it has not started automatically.
7. Wait for the workflow to finish with a green check mark. Open that run, scroll to **Artifacts**, and download `CliporaAI-debug-apk`.
8. Extract the downloaded artifact ZIP. Tap `app-debug.apk` to install it. If Android blocks installation, allow **Install unknown apps** for the browser or My Files app you used, then install only if you trust the build.

Notes:
- GitHub Actions performs the build on GitHub's cloud computer; the phone is used to upload source and download the APK.
- Never commit Gemini/Groq API keys. Add them only inside the installed app's Settings screen.
- This is starter v0.1.0. The current APK has a dashboard and API-key settings, but video download, AI clipping, captions, FFmpeg rendering, and export are not implemented yet.
- Use only source videos you own or are authorized to process. A YouTube URL field does not mean the app downloads YouTube videos.
