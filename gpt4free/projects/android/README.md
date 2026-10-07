# ChatGPT Workspace Android App

This directory contains the Android application for the ChatGPT Workspace project.

## What it does

The app packages the existing g4f-powered chat interface inside a native Android shell. Python runs locally through Chaquopy and the Android WebView connects to the local in-app server at `127.0.0.1:1337`.

Features already wired into the Android shell include:

- Chat UI in WebView
- Local Python backend startup
- Conversation UI supplied by the bundled web application
- File/image picker support
- Runtime microphone and camera permission handling
- Native clipboard bridge
- Browser-automation WebView targets used by supported providers

## Build an APK

From this directory:

```bash
chmod +x ./gradlew
./gradlew assembleDebug --no-daemon
```

The APK is written to:

```
app/build/outputs/apk/debug/app-debug.apk
```

A GitHub Actions workflow also builds the debug APK automatically and publishes it as a workflow artifact.

## Android identity

- App label: ChatGPT Workspace
- Application ID: `dev.dannywise.chatgptworkspace`
- Version: 1.0.0
- Minimum Android version: API 24
- Target/compile SDK: API 34
- Architectures: arm64-v8a and x86_64

This is an independent application and is not an official OpenAI/ChatGPT Android app.

## API keys

Do not put provider API keys inside the APK, source code, or WebView JavaScript. Provider credentials should remain on a server-side backend or be supplied through a secure server-side configuration.

## Current backend model

The Android build currently starts the bundled Python/g4f service locally. Provider availability can change independently of the Android shell, so a future production release should support a configurable HTTPS backend as well.
