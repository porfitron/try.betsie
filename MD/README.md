# Betsie Lite (PWA)

Betsie Lite is a lightweight, serverless web version of the Betsie social betting platform. It is designed to facilitate quick 1-on-1 bets through URL-based state management, allowing users to create, share, and settle bets without creating an account.

## Technical Philosophy
- **Stateless:** Bet data is stored in the URL query parameters. No backend database required for the "lite" experience.
- **PWA First:** Built with vanilla HTML, CSS, and JS. Installable to the home screen with offline-ready properties.
- **Viral Loop:** Focuses on the "Share -> Challenge -> Result" flow via messaging apps (iMessage, WhatsApp, etc.).

## Tech Stack
- HTML5 / CSS3 (Modern Flexbox/Grid)
- Vanilla JavaScript (ES6+)
- Web Manifest & Service Workers for PWA functionality
- Lucide-style SVG icons for a native feel