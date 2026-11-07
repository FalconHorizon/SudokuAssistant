# Sudoku Assistant — Android starter app

This is the first runnable Android Studio project for Sudoku Assistant.

## What works in v1
- Editable 9×9 Sudoku grid
- Example puzzle button
- Clear button
- Offline Sudoku solver (backtracking with minimum-remaining-values selection)
- Duplicate-entry validation and solution display

## Open and run
1. Install Android Studio.
2. Choose **Open** and select this `SudokuAssistant` folder.
3. Let Gradle sync.
4. Connect an Android phone with USB debugging enabled, or use an emulator.
5. Press Run.

## Important scope note
This is the first working app foundation, not yet the screen-scanning / floating-overlay release. The next Android-specific milestones are:
1. Screen capture using Android MediaProjection with explicit user consent.
2. Sudoku grid detection and OCR, followed by a review screen so misread digits can be corrected.
3. Doku Solver website integration (subject to its supported interface and terms; a local solver is already included as a reliable fallback).
4. Optional floating overlay and assisted cell entry. Android restricts overlays and cross-app input, so these require explicit permissions and testing with the target game.

No screen content is captured or transmitted by this starter app.

## Build a free APK with GitHub Actions (phone-friendly)

1. Create a **public** GitHub repository named `SudokuAssistant` (public repositories use standard GitHub-hosted Actions runners at no charge within GitHub's current policy; check your account's Actions limits).
2. Upload the contents of this ZIP to the repository's `main` branch. Make sure the `.github/workflows/android.yml` file is included.
3. Open the repository's **Actions** tab. If prompted, enable workflows.
4. Wait for **Build Sudoku Assistant APK** to finish successfully.
5. Open the completed workflow run, scroll to **Artifacts**, and download `SudokuAssistant-debug-apk`.
6. Extract the downloaded artifact ZIP on your phone. It contains `app-debug.apk`.

This workflow builds a debug APK. Android may ask you to allow installation from the browser or file manager. Only install APKs you built from source you trust.
