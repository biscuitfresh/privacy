# Daily Sudoku Privacy Policy

**Effective Date:** May 31, 2026  
**Last Updated:** May 31, 2026

Daily Sudoku ("**App**", "**we**", "**us**", or "**our**") is a free puzzle game developed by Biscuit Apps. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use our mobile application ("**Daily Sudoku**") on Android devices via the Google Play Store.

Please read this Privacy Policy carefully. By using the App, you agree to the collection and use of information in accordance with this Policy. If you do not agree, please do not use the App.

## 1. Information We Collect

We collect information to provide and improve the core gameplay experience (daily puzzles, leaderboards, progress tracking, and optional premium subscriptions). We do **not** use advertising SDKs, analytics trackers (such as Firebase Analytics), or crash reporting tools (such as Crashlytics).

### 1.1 Information from Google Sign-In (Optional)
If you choose to sign in with Google:
- Email address
- Display name
- Profile photo URL
- Google account identifier (via Firebase Authentication UID)

Sign-in is **optional**. You can use the App fully (including anonymous leaderboard submissions) without signing in.

### 1.2 Pseudonymous Device Identifier ("Install ID")
- We generate and store a random, unique identifier (UUID v4) on your device using local storage.
- This Install ID is sent with game completion submissions to prevent duplicate entries and enable anonymous leaderboard functionality.
- The Install ID is **rotated** (replaced with a new one) after you sign in, so future anonymous play on the same device cannot be linked to your account.
- This identifier is **not** tied to any advertising ID, hardware serial, or personally identifiable device information.

### 1.3 Gameplay and Performance Data
- **Completed puzzle results**: For each daily puzzle you finish, we record:
  - Completion time (in seconds)
  - Number of errors
  - Difficulty level
  - Puzzle date
  - Optional board hash (for basic integrity checking)
- These records are stored in our database and associated with either:
  - Your Install ID (if playing anonymously), or
  - Your user ID (after signing in or via backfill of prior anonymous entries).
- **In-progress game state**: Current board layout, notes, elapsed time, and error count for active puzzles are saved **only locally** on your device using SharedPreferences. This data is never transmitted to our servers.
- **History**: Once signed in, you can view your personal best completion history for past daily puzzles (retrieved from your linked leaderboard entries).

Leaderboard entries (times and errors) are **publicly readable** so that all players can view rankings. No names, emails, or profile information are displayed on public leaderboards.

### 1.4 Subscription and Purchase Information
The App offers optional premium subscriptions ("Daily Sudoku Premium") via monthly and annual plans. All billing is handled exclusively by Google Play Billing.

When you purchase or restore a subscription:
- We receive a purchase token from Google Play.
- The purchase token (along with the product ID) is sent **only to our secure Cloud Function** for verification against the Google Play Developer API.
- On our servers we store a mapping of the purchase token to your Firebase UID, along with basic subscription state (active/expired, expiry time) provided by Google.
- Your user profile is updated with subscription entitlement status (premium tier, status, and expiry date).
- Real-time subscription updates (cancellations, renewals, grace periods) are received via Google Play Real-time Developer Notifications and used solely to keep your entitlement status accurate.

We do **not** receive or store your full payment details, credit card information, or Google Play account credentials. Google handles all financial transactions.

### 1.5 Preference Data
- Theme settings (selected color scheme and light/dark/system mode).
- These are stored locally and, if you are signed in, synced to your user profile so they follow you across devices.

### 1.6 Technical and Usage Information
- Timestamps (e.g., last seen, submission times).
- Basic app version and platform information implicitly collected by Firebase services for operation and security.

We do not collect precise location, contacts, photos (beyond your optional Google profile photo), microphone, camera, or any other sensitive device permissions. The App declares no special Android permissions beyond those required for normal internet connectivity and Google Play services.

## 2. How We Use Your Information

We use the collected information for the following purposes:
- Deliver daily Sudoku puzzles and core gameplay features.
- Maintain accurate, cheat-resistant leaderboards and personal history.
- Provide cross-device access to your completion history and theme preferences when signed in.
- Verify, activate, and maintain premium subscription entitlements (required for Google Play compliance).
- Backfill anonymous leaderboard entries to your account upon sign-in (so your past play is attributed to you).
- Improve the App (e.g., understanding popular difficulties or submission patterns at an aggregate level).
- Enforce security rules and prevent abuse of public leaderboards.
- Communicate with you (if you contact support).

## 3. Legal Bases for Processing (EEA/UK Users)

If you are in the European Economic Area, United Kingdom, or Switzerland, our legal bases for processing include:
- Performance of a contract (providing the game and premium features you request).
- Legitimate interests (operating leaderboards, preventing fraud, improving the service).
- Consent (when you voluntarily sign in with Google or make a purchase).

## 4. Sharing and Disclosure of Information

We do **not** sell your personal information.

We share information only in the following limited circumstances:

- **Google Services (necessary for App functionality)**:
  - Firebase Authentication, Cloud Firestore, and Cloud Functions (Google LLC) — for user accounts, storing profiles, leaderboard data, and subscription verification.
  - Google Sign-In — for authentication.
  - Google Play Billing and Android Publisher API — for in-app purchases and Real-time Developer Notifications.
- **Legal Requirements**: We may disclose information if required by law, court order, or valid government request.
- **Business Transfers**: In the unlikely event of a merger, acquisition, or asset sale, user information may be transferred as part of the transaction.
- **Public Leaderboards**: Puzzle completion times and error counts are publicly visible (associated only with an opaque identifier or your internal user ID; no names are shown).

We do not share data with data brokers, advertising networks, or social media platforms for marketing purposes.

## 5. Data Retention

- **Leaderboard entries**: Retained indefinitely to maintain historical rankings and allow users to view past performance.
- **User profiles**: Retained while your account is active or for a reasonable period after last activity. You can request deletion (see Section 7).
- **Play purchase mappings**: Retained for the duration of the subscription plus a reasonable period afterward to handle refunds, disputes, and re-verification.
- **Local device data** (game saves, Install ID, preferences): Deleted when you clear app data, uninstall the App, or (for Install ID) upon successful sign-in backfill rotation.
- **Anonymous Install ID entries**: Eventually become unlinked from new activity after rotation; old entries remain in leaderboards under the old ID.

## 6. Data Security

We use industry-standard measures to protect your information:
- Firebase Security Rules strictly limit client access (users can only read/write their own profile; leaderboard writes are validated; purchase records are server-only).
- All purchase verification occurs server-side using Google service accounts with minimal required scopes.
- Communication with Firebase and Google Play uses encrypted channels (HTTPS/TLS).
- No sensitive payment data ever touches our servers.

Despite our efforts, no method of transmission or storage is 100% secure. You use the App at your own risk.

## 7. Your Rights and Choices

### Account Controls
- **Sign out**: Stops new data from being associated with your Google account. Previously submitted anonymous entries remain under the rotated Install ID.
- **Delete local data**: Clear the App's cache/storage in your device settings or uninstall the App.
- **Theme and game progress**: Managed entirely locally until you sign in.

### Access, Correction, and Deletion
- You can view your linked completion history inside the App after signing in.
- To request access to, correction of, or deletion of your personal data (user profile, linked leaderboard entries, purchase records), please contact us (see Section 10). We will respond within a reasonable time and in accordance with applicable law (including GDPR/CCPA/CPRA where applicable).
- Note: Deleting your account will remove your user profile and subscription status. Public leaderboard entries you previously submitted will remain (anonymized or under your former user ID) as they form part of the historical record for all players. If you want specific entries removed, include that detail in your request.

### Subscription Management
- Cancel or manage subscriptions directly in the Google Play Store under your account subscriptions.
- Restoring purchases is supported inside the App.

### Opt-Out of Sign-In
You may use every feature of the App, including submitting scores to leaderboards, without ever signing in.

## 8. Children's Privacy

Daily Sudoku is a general-audience puzzle game suitable for players of all ages, including children.

We do not knowingly collect personal information from children under 13 (or the applicable age of digital consent in your jurisdiction) in a way that would require parental consent under COPPA or similar laws, beyond what is strictly necessary for basic gameplay functionality.

- Sign-in with Google is optional and subject to Google's own age-appropriate consent flows.
- No advertising or behavioral tracking occurs.
- If you believe we have inadvertently collected information from a child under 13, please contact us immediately so we can delete it.

## 9. International Data Transfers

Your information may be transferred to and processed in the United States and other countries where Google Firebase and our infrastructure providers operate. These countries may have different data protection laws than your jurisdiction. By using the App, you consent to such transfers. We rely on appropriate safeguards (such as Google's standard contractual clauses) where required.

## 10. Contact Us

If you have questions, concerns, or requests regarding this Privacy Policy or our data practices, please contact us:

- Through the Google Play Store listing for Daily Sudoku (preferred for fastest response)
- Email: biscuitappscontact@gmail.com (replace with your real support address before publishing)

We will respond to verified requests as promptly as possible.

## 11. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. When we do, we will revise the "Last Updated" date at the top of this document and, where appropriate, notify users via an in-App notice or updated Play Store listing.

Your continued use of the App after any changes constitutes acceptance of the revised Policy.

## 12. Additional Information for Specific Jurisdictions

- **California (CCPA/CPRA)**: We do not sell personal information. You have the right to know what information we collect, request deletion, and opt-out of any future "sale" (we currently have none). Contact us to exercise these rights.
- **EEA / UK / Switzerland (GDPR/UK GDPR)**: You have rights to access, rectification, erasure, restriction, portability, objection, and to lodge a complaint with your local supervisory authority.
- **Brazil (LGPD)**: Similar rights apply. Contact us for requests.

---

**Summary for Google Play Store reviewers**:  
Daily Sudoku collects only the minimal data necessary for gameplay (optional Google profile for sign-in, pseudonymous game results for leaderboards and history, and purchase tokens solely for Google Play subscription verification). No advertising, analytics, or unnecessary tracking occurs. All sensitive operations use Google's secure services and our tightly scoped security rules.

This document is provided as a starting point based on the App's actual code and data flows. **Customize the developer name, contact email, effective date, and any additional details before making it publicly available.** Host the final version at a permanent public HTTPS URL and enter that URL in the Google Play Console under **App content > Privacy Policy**.

---

*© 2026 Biscuit Apps. All rights reserved.*