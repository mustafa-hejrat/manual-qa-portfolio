# Password Recovery — Manual Test Cases

## 1. Test Objective

Verify that users can access the password recovery feature successfully and that the application handles invalid input, navigation, and network issues appropriately.

## 2. Test Information

- **Feature:** Forgot Password
- **Application:** thePersonal mobile app
- **Platform:** Android
- **Test Type:** Functional, Negative, Navigation, and Error Handling
- **Test Status:** Not Executed
- **Related Bug:** [MANUAL-001 — Forgot Password Navigation Error](../bug-reports/forgot-password-android.md)

## 3. Test Cases

### TC-001: Open the Password Recovery Page

**Priority:** High  
**Type:** Positive / Navigation

**Preconditions:**
- The application is installed and open.
- A password prompt is available.

**Steps:**
1. Navigate to the Edit section.
2. Enter an incorrect password to display the password prompt.
3. Tap **I Forgot My Password**.

**Expected Result:** The password recovery page opens successfully without displaying a navigation error.

**Actual Result:** Not recorded — test not executed.

**Status:** Not Executed

---

### TC-002: Open Password Recovery from the Documents Section

**Priority:** High  
**Type:** Navigation / Regression

**Steps:**
1. Navigate to the Documents section.
2. Trigger the password prompt.
3. Tap **I Forgot My Password**.

**Expected Result:** The password recovery page opens successfully.

**Actual Result:** Not recorded — test not executed.

**Status:** Not Executed

---

### TC-003: Submit a Valid Email Address

**Priority:** High  
**Type:** Positive / Functional

**Preconditions:**
- The password recovery page is accessible.
- A registered test email address is available.

**Steps:**
1. Open the password recovery page.
2. Enter a registered email address.
3. Submit the recovery request.

**Expected Result:** The application displays an appropriate confirmation message and follows the documented password recovery process.

**Actual Result:** Not recorded — test not executed.

**Status:** Not Executed

---

### TC-004: Submit an Invalid Email Address

**Priority:** Medium  
**Type:** Negative / Validation

**Steps:**
1. Open the password recovery page.
2. Enter an invalid email format, such as `user@`.
3. Submit the request.

**Expected Result:** The application displays a clear validation message and does not submit an invalid email address.

**Actual Result:** Not recorded — test not executed.

**Status:** Not Executed

---

### TC-005: Submit an Empty Email Field

**Priority:** Medium  
**Type:** Negative / Validation

**Steps:**
1. Open the password recovery page.
2. Leave the email field empty.
3. Submit the request.

**Expected Result:** The application prompts the user to enter an email address and does not submit the empty form.

**Actual Result:** Not recorded — test not executed.

**Status:** Not Executed

---

### TC-006: Handle Network Unavailability

**Priority:** Medium  
**Type:** Error Handling

**Steps:**
1. Open the password recovery page.
2. Disable the device's network connection.
3. Submit a recovery request.

**Expected Result:** The application displays a clear network-related message and provides an appropriate way to retry when connectivity returns.

**Actual Result:** Not recorded — test not executed.

**Status:** Not Executed

---

### TC-007: Return to the Previous Screen

**Priority:** Low  
**Type:** Navigation

**Steps:**
1. Open the password recovery page.
2. Use the app's Back button or Android system Back action.

**Expected Result:** The application returns to the appropriate previous screen without crashing or displaying an unexpected error.

**Actual Result:** Not recorded — test not executed