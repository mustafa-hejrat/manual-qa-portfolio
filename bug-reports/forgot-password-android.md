# Bug Report: Forgot Password Navigation Error on Android

## Bug Details

- **Bug ID:** MANUAL-001
- **Application:** thePersonal mobile app
- **Platform:** Android
- **Module:** Document Editing / Documents
- **Bug Type:** Functional / Navigation
- **Severity:** Medium (proposed)
- **Priority:** P2 (proposed)
- **Status:** New

## Description

When a user enters an incorrect password while trying to edit or access a document and taps **"I Forgot My Password,"** the app displays a "Web page not available" error instead of opening the password recovery page.

The issue was observed in both the Edit and Documents sections.

## Preconditions

- The thePersonal mobile app is installed on an Android device.
- The user can access the Edit and Documents sections.
- A password prompt appears when attempting to edit or access a document.

## Steps to Reproduce

1. Open the thePersonal mobile app on an Android device.
2. Navigate to the Edit section.
3. Enter an incorrect password when prompted.
4. Tap **"I Forgot My Password."**
5. Observe the resulting screen.
6. Repeat the test in the Documents section.

## Expected Result

The app opens the password recovery page and allows the user to begin resetting their password.

## Actual Result

The app displays a "Web page not available" error instead of opening the password recovery page.

**Observed error:**

`net::ERR_UNKNOWN_URL_SCHEME`

## User Impact

Users who forget their password may be unable to access the password recovery flow from the Edit and Documents sections, potentially preventing them from completing document-related tasks.

## Technical Investigation Note

The error suggests that the Android WebView is attempting to navigate to a URL scheme it does not recognize or handle. The development team should investigate the password recovery link format and the app's handling of this navigation action. This is a suspected area for investigation, not a confirmed root cause.

## Regression Test Recommendation

Verify that tapping **"I Forgot My Password"** from both the Edit and Documents sections opens the correct password recovery page without displaying a navigation error.

## Test Evidence

- **Evidence type:** Screenshot
- **Platform:** Android
- **Observed error:** `net::ERR_UNKNOWN_URL_SCHEME`
- **Screenshot:** [View screenshot](../test-evidence/Screenshot_forgot-password-error.jpg)

## Notes

Severity and priority are preliminary assessments and may be adjusted based on business impact and the availability of alternative password recovery methods.