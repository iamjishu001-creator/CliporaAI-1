# Clipora AI — Android starter project

A clean-room Android starter for an ad-free AI Shorts creator, inspired by the feature set discussed with the user. It does not copy the original APK's source code or proprietary assets.

## Current status (v0.1.0)
- Jetpack Compose dark dashboard
- YouTube URL input and basic URL validation
- Settings screen for Gemini and Groq API keys
- API keys stored with AndroidX EncryptedSharedPreferences
- No advertising SDK, AdMob dependency, banner, interstitial, rewarded-ad flow, or ad unlock logic

## Not implemented yet
- Fetching/downloading source video
- AI transcript and viral-moment ranking
- Gemini/Groq network clients
- Speech-to-text and caption timing
- FFmpeg clip rendering and 9:16 export
- Gallery save/share and job history

These modules are deliberately marked as pending in the UI; this starter does not pretend that video processing already works.

## Build
1. Open this folder in Android Studio (recent version with Android Gradle Plugin 8.13 support).
2. Install Android SDK 36 and JDK 17.
3. Sync Gradle.
4. Run the `app` configuration on an Android device (min SDK 26).

## Important implementation notes
- The app has no ad SDK and contains no ad-related permissions or code.
- Keep personal API keys private. For a public release, route AI requests through a backend so keys are not embedded in the APK. Local encrypted storage is suitable only for a personal-use build.
- YouTube URL support is only a validated input at this stage. A compliant source-media workflow must be designed before downloading or processing videos; users should only process videos they own or are authorized to use.
