# Product Requirements: Betsie Lite

## 1. Goal
Position Betsie Lite as a backend-less head unit for a user's preferred chat platform (iMessage, SMS, or WhatsApp), providing a friction-free way to create and settle 1-on-1 social bets through a single link. Encourage users to upgrade to the full iOS app for persistent history and global leaderboards.

## 2. Product Positioning
- **What Betsie Lite is:** A share-first, no-account, no-backend control surface for social bets.
- **What chat apps do:** Handle identity, delivery, thread context, notifications, and re-engagement.
- **What Betsie Lite does:** Handle bet composition, link state, challenge acceptance, countdown, and settlement UI.
- **What this means for UX:** Every screen should optimize for "send this into chat now" and "re-open from chat later."

## 3. Core User Flows
### Flow A: The Creator
1. User opens the PWA.
2. User enters: Bet Title, Their Position (Yes/No or Custom), and Deadline.
3. App generates a "Challenge Link" (e.g., `betsie.app/?t=Marathon+Goal&p1=Yes&d=2026-05-01`).
4. App presents channel-aware share copy that works in iMessage, SMS, or WhatsApp.
5. User shares the link into an existing chat thread.

### Flow B: The Challenger
1. Friend opens the link.
2. Friend sees the bet details and a "Accept Challenge" button.
3. Friend selects the opposing position.
4. The URL updates to include the Challenger's state (e.g., `&p2=No`).
5. Friend shares the updated link back into chat with one tap.

## 4. Key Features
- **URL-Encoded State:** All bet details (title, positions, dates) are parsed from and written to the URL.
- **Channel-Aware Share Copy:** Prebuilt, concise share text that reads naturally in iMessage, SMS, and WhatsApp.
- **Re-open Resilience:** Opening the same link later should restore context with no confusion and no required login.
- **Countdown Clock:** A real-time visual timer showing hours/minutes/seconds until the bet deadline.
- **Add to Calendar:** A button to generate an .ics file or Google Calendar link for the bet deadline.
- **Results Page:** After the deadline passes, the UI transitions to a "Settlement" mode with a fanfare animation (confetti) for the winner.
- **iOS Upsell:** Persistent banners and "locked" features (History, Profile, Win/Loss Record) that link to the App Store.

## 5. UI/UX Requirements
- **Mobile-First:** Styled to look like a native iOS/Android app.
- **The "Vibe":** Energetic, social, and clean. Use high-contrast buttons and playful typography.
- **Head-Unit Mental Model:** The app should feel like a quick control panel, not a destination social feed.
- **Fast-to-Share:** Primary CTA on all pre-settlement screens should be sharing back into chat.
- **Cross-Channel Clarity:** Copy must avoid platform-specific jargon and still feel native in iMessage/SMS/WhatsApp contexts.
- **Public Visibility:** Bets are public by URL design; no "Discover" feed helps preserve pseudo-privacy.

## 6. Content Guidelines
- Keep microcopy short enough to survive message previews and link unfurls.
- Default to plain-language actions: "Create", "Share", "Accept", "Settle".
- Avoid internal product terms (for example, "stateful URL") in user-facing text.
- When possible, generate share text with a clear challenge + deadline + call-to-action pattern.

## 7. Messaging Constraints (Chat-First)
- **Creator invite share format:** `creator claim` + optional `trash talk hook` + link.
- **Default hook when blank:** "Prove me wrong."
- **Do not expose "YES/NO" language in outbound creator invite text.**
- **Character limits (hard):**
  - Creator name: 20
  - Challenger name: 20
  - Claim/position text: 70
  - Trash talk (creator/challenger): 45
  - Challenger custom position text: 70
- **Share copy budget target:** Keep pre-link message text concise (generally <=160 chars) for readability in iMessage/SMS/WhatsApp threads.