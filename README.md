# Nexa CRM Android (clean repository layout)

This repository is laid out as a Gradle Android project at the repository root so GitHub Actions does not need to download or unzip a nested source archive.

## Build APK with GitHub Actions

1. Upload the contents of this folder to a GitHub repository (the `.github/workflows/android.yml` file must be included).
2. Open the repository's **Actions** tab.
3. Choose **Build Nexa CRM APK** and run **Run workflow**, or push a commit.
4. When the run succeeds, open the run and download the `NexaCRM-debug-APK` artifact.

## Current application limitations

This source is a prototype. The Android activity wraps the web interface, and sharing text into the app is supported by the Android activity. The existing HTML currently describes local browser storage and prototype behavior. Do not treat this package as proof that secure account login, cross-device Supabase sync, automatic WhatsApp reading, AI summaries, or notifications are fully implemented or tested. Those features need implementation and testing before production use.

## Supabase

The SQL setup file is included as a starting point only. Never put a Supabase `service_role` key in the Android app. Only use a publishable/anon key with appropriate row-level security policies.
