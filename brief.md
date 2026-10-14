Version: NAFATH-V1
Track: Networking

## Overview
The single sign-on service combines six disciplines around one citizen login. Software engineering builds it on OpenID Connect, which handles user authentication, while OAuth 2.0 only delegates access to resources. On Android, the app is sandboxed and requests dangerous permissions, such as the camera, at runtime and only when a user action needs them. Networking uses DNS over HTTPS to encrypt DNS lookups against eavesdropping and tampering, though it does not hide the destination server or replace TLS. Cybersecurity requires phishing-resistant authentication such as passkeys (FIDO2/WebAuthn), unlike SMS codes or one-time passwords. AI fraud detection must be governed under a framework like NIST AI RMF, addressing bias, false positives, deepfakes, and explainability before launch. Data handling follows Oman's Personal Data Protection Law: consent, notice, a data protection officer, breach notification, and restricted transfers abroad.

## Software
OAuth 2.0 is a delegated authorization framework that lets an application access protected resources, such as files or contacts, on a user's behalf using an Access Token. OpenID Connect (OIDC) is an identity layer built on top of OAuth 2.0 that handles authentication, verifying who the user is through an ID Token. In a government program, OIDC provides single sign-on through the national digital identity, while OAuth 2.0 ensures each agency's service accesses only the data the citizen authorized.

Resource: OAuth 2.0 Simplified - OAuth.com - https://www.oauth.com/oauth2-servers/openid-connect/authorization-vs-authentication/

## AI
Under the NIST AI Risk Management Framework, the authority must manage risks including bias against certain groups, threats to data privacy and its centralization, wrong decisions that are hard to explain, and misuse in deepfakes and cyberattacks. Systems should be tested before launch and monitored continuously; data collection should be minimized and protected; final decisions should remain with humans, with appeals and alternatives available; and a responsible party should be assigned to each service.

Resource: Artificial Intelligence Risk Management Framework (AI RMF 1.0) - https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf

## Mobile
Android enforces application sandboxing, restricting each app to its own resources unless access is granted. On Android 6.0 (API 23) and above, dangerous permissions such as CAMERA must be requested at runtime; a manifest declaration alone is insufficient. The login app should request each permission contextually, only when a user action requires it (for example, scanning a QR code), verify permission status before accessing the resource, and provide a fallback, such as manual code entry, if access is denied.

Resource: Request runtime permissions - https://developer.android.com/training/permissions/requesting

## Networking

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
