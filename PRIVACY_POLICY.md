# Privacy Policy — Airport Shuttle Tracker (Driver & Passenger)

Last updated: 2025-09-28

Welcome to the Airport Shuttle Tracker app for Android. This app provides two variants from a single codebase:

- Driver: `com.example.airportshuttle.driver`
- Passenger: `com.example.airportshuttle.passenger`

We take your privacy seriously. This policy explains what data we collect, how we use it, and your choices.

- No data is sold to third parties.
- Only the minimum data necessary to deliver core functionality is used.

## Data Controller

- App name: Airport Shuttle (Driver & Passenger)
- Platform: Android
- Contact: airportshuttletracker@gmail.com

## Scope of this policy

This policy applies to both variants:

- Driver: shares live location to help passengers track arrivals.
- Passenger: views selected driver location updates on a map.

## Data we collect and why

- **Account and profile data (Driver and optional Passenger with sign-in)**
  - What: Email, user ID, optional display name.
  - Why: Authentication, user identification, and secure access control.
  - Where: Stored in Firebase Authentication and Firestore.

- **Driver live location (Driver variant only)**
  - What: GPS coordinates and timestamp while sharing is ON.
  - Why: To show the driver’s location in near real-time to the selected passenger(s).
  - Where: Stored/transmitted via Firebase Realtime Database (RTDB), typically with short-lived retention or as your app defines.

- **Push messaging tokens (FCM)**
  - What: Firebase Cloud Messaging (FCM) registration token.
  - Why: To send service notifications (e.g., status updates).
  - Where: Stored in Firestore as part of the user profile.

- **App preferences and UI state**
  - What: Non-sensitive settings (e.g., theme).
  - Where: Stored locally on device.

- **Diagnostics and crash logs**
  - What: Minimal logs to troubleshoot issues (if enabled by your device settings).
  - Why: Improve reliability and performance.

We do not collect sensitive categories of personal information (e.g., political opinions, health data) and we do not build advertising profiles.

## How we use your data

- Provide core functionality (location sharing, map display).
- Authenticate users and secure access.
- Communicate essential service messages (e.g., push notifications).
- Improve reliability and safety (diagnostics).

## Legal bases (where applicable)

- Consent: for location sharing (Driver must explicitly start sharing).
- Contract: to provide app services you request.
- Legitimate interests: app security, fraud prevention, and essential communications.

## Third-party services and links

We use the following providers to deliver core functionality. Refer to their privacy policies:

- Firebase (Auth, Firestore, Realtime Database, Cloud Messaging)
  - https://firebase.google.com/support/privacy
- Google Play services and Google Maps Platform
  - https://policies.google.com/privacy
- Google Maps SDK for Android and related APIs
  - https://developers.google.com/maps/terms

These services may process data (e.g., IP address, device identifiers) required for connectivity, security, and service operations.

## Data storage and retention

- Driver locations: stored in RTDB while sharing is active; retention is minimal and controlled by the app logic or your administrative policy. You may stop sharing anytime.
- Account data: retained while your account exists. You may request deletion (see “Your choices and controls”).
- Preferences: stored locally; deletion occurs upon app data clear or uninstall.

## Data sharing

- Driver location is shared only with intended recipients inside the app (e.g., selected passengers) to fulfill the tracking feature.
- We do not sell personal data.
- We share data with infrastructure providers (Firebase/Google) strictly to deliver app functionality.

## Children’s privacy

This app is not directed to children under the age where parental consent is required by local law. If you believe a child has provided personal data without consent, contact us to remove it.

## Permissions used and purpose

Driver and Passenger share many permissions, but intent differs by variant.

- `ACCESS_FINE_LOCATION` / `ACCESS_COARSE_LOCATION` (Driver & Passenger)
  - Driver: obtain precise location to share while tracking is ON.
  - Passenger: enable My Location layer on the map (optional).
- `FOREGROUND_SERVICE` (Driver)
  - Keep location updates alive while the driver shares location.
- `POST_NOTIFICATIONS` (Android 13+, Driver & optional Passenger)
  - Display service-related notifications.
- `INTERNET` / `ACCESS_NETWORK_STATE` (Driver & Passenger)
  - Access Firebase/Maps services.
- `RECEIVE_BOOT_COMPLETED` (Driver)
  - Optionally restore driver service states after device reboot (if implemented).

Note: The full set of permissions is declared in `app/src/main/AndroidManifest.xml`. You can revoke optional permissions in Android Settings at any time. Some features may not work without the corresponding permission.

## Your choices and controls

- **Driver location sharing**: You explicitly start/stop sharing in the app. When OFF, no new location updates are sent.
- **Access and correction**: You may view and update your profile details (where implemented).
- **Deletion**:
  - Delete local data by uninstalling the app or clearing app data.
  - Request account/cloud data deletion by contacting support (see “Contact”).
- **Notifications**: Toggle app notification permissions in Android Settings.

## Security

We implement reasonable technical measures (e.g., Firebase security rules, authenticated access, HTTPS/TLS) to protect data in transit and at rest. No system can guarantee 100% security.

## International data transfers

Data may be processed and stored on servers located outside your country, including in regions where Firebase/Google services operate. By using the app, you acknowledge such transfers as necessary to provide the service.

## Changes to this policy

We may update this policy from time to time. Material changes will be reflected here with an updated “Last updated” date. Continued use of the app indicates acceptance of the revised policy.

## Contact

If you have questions about this policy, privacy, or data requests, contact:

- Email: airportshuttletracker@gmail.com
