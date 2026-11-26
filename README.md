# CodeNova: Sahayak

**Team CodeNova** | PRAYAS 2026 | Student category
**Sneha Sharma**, B.Tech 3rd year, Graphic Era Hill University, Dehradun

Sahayak is a voice-first assistant that helps citizens file a CM Helpline complaint by simply talking. It is built for elderly citizens, first-time smartphone users and people in remote hill villages, where long formal forms and weak signal make filing hard.

**[Open the live prototype](https://snehasharmaa912-ops.github.io/CodeNova/prototype/)**

## Files

- `CodeNova.pptx`: pitch deck
- `prototype/index.html`: clickable prototype (open it in a browser)
- `prototype/sw.js`: service worker that lets the prototype load offline

## Try the prototype

The prototype runs the full citizen journey in three steps, plus a service helper:

1. **Speak or type** the problem in Hindi or English (voice works in Chrome on Android and desktop; otherwise type, or tap "Fill an example").
2. **Check the complaint.** The department is suggested from what was said, and the citizen can add location and a photo.
3. **Track it.** A status timeline shows progress, and "Show next update" simulates the SMS alerts.

Also in the prototype:

- **Explainable routing.** The review screen shows the suggested department, a confidence level (high, medium, low) and the words that led to it. The citizen can change it.
- **Urgent cases.** Words like fire, sparking, accident or flood mark the complaint urgent and show "call 112" for anyone in danger. Duration ("since two days") is picked up too.
- **Read aloud.** A button reads the complaint and department back, for citizens who find reading hard.
- **Accessibility controls.** Three text sizes and a high-contrast mode, remembered on the phone.
- **Duplicate flagging.** After adding a location, the citizen sees that similar complaints exist in the area and that theirs will be linked to them (sample figures).
- **Smart follow-ups.** If the citizen forgets where or since when, the review screen asks, with one-tap choices ("Since today", "Since this week", "Over a month") and an "Add my location" button.
- **Photo compression.** A photo is shrunk on the phone before sending (for example 5.7 MB to about 260 KB), which helps on weak networks.
- **Track a complaint.** Look up a complaint by reference number, or pick from the complaints on this phone. A "Share status on WhatsApp" link lets a family member follow along.
- **Privacy screen.** Plain-language note on what is kept, and a button that deletes all data from the phone. The prototype's voice input uses the browser's own speech service, and the screen says so.
- **Offline drafts.** What the citizen types is saved on the phone as they go and comes back after a reload. Tap "Simulate weak signal" (or use airplane mode), submit, and the complaint is held on the phone and sent automatically when signal returns. A service worker (`sw.js`) keeps the page itself loading with no network after the first visit.
- **Officer view (demo).** A department chart and complaints that arrive clean, with department, urgent, duplicate, photo and location flags. Moving a complaint to the next stage updates the citizen's timeline and the WhatsApp/SMS alert preview.
- **Which service do I need?** Tells the citizen whether their need is an Apuni Sarkar service (links to eservices.uk.gov.in) or a complaint to file with Sahayak. The list is an example.

> This is a prototype. Speech and department suggestions run in the browser with simple keyword matching. Routing, duplicate counts and the officer view use simple rules and sample data. Offline saving uses the browser's local storage (the photo itself is not stored yet). Nothing is sent to CM Helpline, and the departments shown are examples.

## What the full version adds

- Garhwali and Kumaoni voice support, after Hindi
- LLM-based complaint summary and department routing
- Offline drafts with photos, synced in the background when the signal returns
- SMS and WhatsApp alerts
- Duplicate detection and an officer dashboard
- Integration with the existing CM Helpline workflow

## Plan

| Month | Focus |
|-------|-------|
| 1 | Prototype and Hindi voice-to-complaint demo |
| 2 | Garhwali and Kumaoni samples, pilot with real users |
| 3 | CM Helpline integration and WhatsApp alerts |

## Contact

snehasharmaa912@gmail.com
