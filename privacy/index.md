---
title: Woven Privacy Policy
permalink: /privacy/
render_with_liquid: false
---

# Woven Privacy Policy

Effective November 1, 2026

Woven is an iPhone, iPad and Apple Watch app for training plans, workout logging, an AI training coach and heart-rate broadcasting. It is built by an independent developer ("we", "us"). This policy explains what Woven handles, where that data goes and the choices you have.

## Summary

- Woven has **no account system and no Woven server**. Your training data is stored on your devices.
- Apple Health data is read only with your permission. It is never used for advertising, marketing or data mining, and it is never sold.
- The AI coach sends your conversation and training context to **the AI provider you connect**, such as OpenAI. The Apple Health summary and readiness check-ins are included only if you turn on **Share Health context with Coach**.
- **Share usage & diagnostics** sends privacy-filtered app diagnostics to PostHog. It is **off by default** in TestFlight and App Store builds.
- Woven has no ads, does not track you across apps or websites, and does not sell or rent personal data.

## Data stored on your devices

Woven stores the following in its app container on your device. Some items are also stored in its App Group so that its widgets and Live Activities can read them.

- Your training profile: goal, schedule, experience, equipment, available load, limitations and any notes you add.
- Plans, coach conversations, workout logs (the Journal), readiness check-ins and timers.
- Heart-rate broadcast history, including heart-rate samples, and heart-rate zone settings.
- Preferences and the AI provider and model you chose.

This data is written with iOS file protection. Woven does not send it to us. Like other app data, it can be included in your device backups, depending on how you have set up your device's backup.

Widgets, Live Activities and the Watch app can show your heart rate, workout and plan on your Lock Screen, Home Screen and watch face.

## Apple Health

With your permission, Woven reads:

- heart rate, to broadcast it and show it during workouts
- workouts from the last 14 days, for training history
- sleep, resting heart rate, heart rate variability (SDNN), respiratory rate, blood oxygen, sleeping wrist temperature, cardio fitness (VO₂ max) and 1-minute heart-rate recovery, for training context

Woven runs a workout session to collect continuous heart rate, mainly on Apple Watch. It saves a workout to Apple Health only when you choose to save it.

Woven reads most Health data only when it needs to show it or build coaching context. It keeps these Health-derived values on your device:

- **Workout and broadcast heart rate**: heart-rate samples recorded during a broadcast or workout are saved in your broadcast history, with average and maximum heart rate and time in each zone.
- **Heart-rate zones**: when Woven has Health access, it saves your latest Health resting heart rate with its zone settings. If you use Health for your zones, it also saves your preferred Health heart-rate zones.
- **Link and save**: if you link an Apple Health workout to a planned session, Woven saves that workout's identifier, source app, start time and duration in your Journal entry.
- **Save to Apple Health**: when you save a Woven workout to Apple Health, Woven records the new Health workout's identifier and activity type in the Journal entry.
- **Plan reviews**: when **Share Health context with Coach** is on, the latest summary of the readings above may be saved with Woven's local coaching data. This stops the coach from repeating a plan review for unchanged data.

All of these stay on your device and are erased by **Reset Woven**.

You can change Woven's Health access at any time in the Health app or in **Settings → Apple Health**.

Woven never uses Health data for advertising, marketing or data mining. It shares Health data only in these cases, and only after you choose to:

- **With your AI provider**, when **Share Health context with Coach** is on. Separately, details of Health workouts you linked or saved are part of your Journal entries, and recent entries are sent whenever you use the coach. See the next section.
- **Over Bluetooth**, when you start a heart-rate broadcast. See "Bluetooth" below.

## AI coaching providers

The coach runs on an AI provider that **you** connect in **Settings → Coach**:

- **ChatGPT plan**: you sign in with your OpenAI account in a secure browser sheet.
- **OpenAI API, Anthropic, OpenRouter** or a **custom endpoint**: you provide an API key.

Woven asks for your permission before sending any requests to a provider: **Allow requests using my ChatGPT plan**, or **Allow coaching requests to** your API provider. Woven sends requests directly from your device to the provider; they do not pass through any Woven server.

Woven sends the provider the following when you message the coach. It also sends it automatically when you return to the app with a saved plan, a connected provider and changed training data, so the coach can check your plan. Automatic checks don't run with the Demo coach or during a workout.

- up to 30 recent conversation messages, including your messages and the coach's earlier replies
- your training profile (goal, schedule, experience, equipment, load, limitations, travel and other notes you provide)
- your current plan, including workouts you have completed in it, and any draft plan
- your five most recent Journal entries: the exercises and sets you performed, your feedback and timing, and the Health details described above for workouts you linked or saved to Apple Health
- today's date

Only if **Share Health context with Coach** is on, Woven also sends:

- a summary of your recent Apple Health workouts (type, duration, date and source app)
- the latest values of the Health readings listed above, with their dates and sources
- your current self-reported readiness score and note

Health context sharing is a separate choice that is off until you turn it on. It is also turned off when you change or disconnect a provider.

The provider's own terms and privacy policy govern how it handles this data. Some providers, such as OpenRouter, forward requests to other model providers under their own terms. When you use a ChatGPT plan, Woven asks OpenAI not to store responses (`store: false`). OpenAI may still keep data under its own policies, for example for abuse monitoring.

The **Demo coach** runs entirely on your device and sends nothing to any provider.

AI providers are independent services. You choose them and use them under your own agreement with them. Woven sends them data only after you connect them and allow requests, and only to provide the coaching you ask for. Review a provider's privacy policy before you connect it, especially a custom endpoint.

AI output can be wrong. Woven's coach is not medical advice. Check with a doctor before you start or change a training program, especially if you have an injury or a medical condition.

## Credentials

ChatGPT sign-in tokens and provider API keys are stored in the iOS Keychain on this device only. They are not restored to a different device from a backup. They are sent only to the provider that issued them.

ChatGPT sign-in gives Woven your OpenAI account's email address and account identifier. Woven uses them on the device to show which account is connected and to keep each account's model choice separate. We never receive them.

To remove credentials:

- Use **Disconnect ChatGPT** or **Disconnect provider** in **Settings → Coach**.
- Or use **Reset Woven**.
- You can also revoke access, or delete your API keys, in your provider account.

## Bluetooth

When you start a broadcast, Woven advertises a standard Bluetooth Heart Rate Service named "Woven". This lets workout apps and equipment near you show your heart rate. Like other heart-rate sensors, **any nearby device can receive the broadcast heart rate while broadcasting is on.** Stop broadcasting to end it.

Woven can also connect to a Bluetooth heart-rate sensor you choose. Device names and identifiers stay on your device.

## Exercise videos

Exercises can include a video link, added by you, by the coach or by a plan. When you play or open a video, Woven connects directly to YouTube or to the HTTPS host in the link. That service receives your IP address and the requested video, and handles them under its own privacy policy.

## Apple Watch

The Watch app runs workouts and gets heart rate from Apple Health. It exchanges workout and plan data with your paired iPhone using Apple's Watch Connectivity.

The Watch app does not contain an analytics SDK. If you turn on diagnostics, it may queue up to 64 diagnostic records for up to 7 days for the iPhone app to send. Turning diagnostics off clears that queue.

## Optional usage and diagnostics (PostHog)

**Share usage & diagnostics** is in the first-run setup and in **Settings → Privacy & diagnostics**. It is off by default in TestFlight and App Store builds. When it is on, the iPhone and iPad app sends diagnostics to [PostHog](https://posthog.com/privacy), our analytics service provider, using PostHog's US cloud. PostHog processes this data on our behalf to help us find and fix problems.

**What it sends**

- App opens, setup completion and fixed-name actions, such as "plan review opened" or "training profile confirmed".
- Broadcast, relay and Health diagnostics: whether operations succeeded, their timing and categorized errors. Readings are not included.
- Coach request diagnostics:
  - stages, timing and HTTP status
  - categorized errors
  - provider request IDs
  - the requested, resolved and returned model names
  - token counts
  - tool-call outcomes
- Crash reports: stack traces, app and OS version, and device model.
- A random installation identifier, plus random IDs for each diagnostic attempt.

Diagnostics may also include coarse operational details: app lifecycle and low-power state, connection and delivery counters, and response format, size and stream-event categories. They never include response content.

**What it never sends**

- Your prompts, coach replies, plans, goals or notes.
- Tool inputs or outputs.
- Health readings or records, heart-rate values or zone thresholds.
- Device or sensor names, Bluetooth identifiers or exact workout durations.
- Email addresses, account identifiers or credentials.

Screen recording, session replay, automatic tap capture, surveys and location enrichment are disabled. Like any internet service, PostHog receives your IP address when the app connects. We do not use it to locate or identify you.

Diagnostics are pseudonymous. They are linked to the random installation identifier, not to your name or email. We use them only to operate and improve Woven. We do not use them for advertising and do not combine them with other data to identify you.

PostHog is our service provider and processes diagnostics only on our behalf. We require service providers that receive Woven data to protect it at least as well as this policy does.

## How long data is kept, and how to delete it

**On your device**

- Your data stays until you delete it.
- **Settings → Reset Woven** erases the following and turns diagnostics sharing off:
  - plans, conversations, workout and broadcast history, profile, timers and preferences
  - saved connections on that device
- Deleting the app removes its local data. iOS may keep Keychain items after an app is deleted, so disconnect your provider first to remove its credentials.
- Reset does not delete your Apple Health records or your accounts with AI providers.

**Diagnostics**

- Turning off **Share usage & diagnostics** stops all new uploads immediately. It does not delete data PostHog has already received.
- We keep diagnostics only as long as they help us diagnose and improve Woven. PostHog deletes events automatically at the end of its retention period: 1 year on PostHog's free plan and up to 7 years on paid plans.
- To ask us to delete your diagnostics, contact us (see below). Include the **Latest diagnostic** ID if you have one; it appears in **Settings → Privacy & diagnostics** after a problem. Because diagnostics are not linked to your identity, we need an identifier like this to find your records.

**AI providers**

Data sent to an AI provider is handled under that provider's retention policies. Use your provider account to manage or delete it. For example, ChatGPT usage can be managed at chatgpt.com.

## Security

Woven's network connections to AI providers, PostHog and exercise video hosts use HTTPS. It uses iOS file protection for local data and the Keychain for credentials. Diagnostics are filtered so that only allowlisted fields are sent. No method of storage or transmission is perfectly secure, but we design Woven to keep as little data off-device as possible.

## Children

Woven is not directed to children under 13, or the minimum age in your country. We do not knowingly collect personal data from children. Woven does not collect names, birthdates or contact details itself. If you believe a child's data has been sent to us through diagnostics, contact us and we will delete it.

## Your rights

Depending on where you live, you may have rights to access, correct, delete or object to the processing of your personal data. Most Woven data never leaves your device, so you can view, change or erase it directly in the app. For diagnostics held by PostHog on our behalf, contact us using the method below.

## Changes

If we change how Woven handles data, we will update this policy and its effective date. We will ask for your consent in the app before any new use of your data that needs it.

## Contact

For privacy questions or deletion requests:

- **TestFlight testers**: use **Send Beta Feedback** in TestFlight, or the feedback email shown on Woven's TestFlight page.
- **App Store users**: use the support link on Woven's App Store page.
