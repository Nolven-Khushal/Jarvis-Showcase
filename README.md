<p align="center">
  <img src="screenshots/00-logo.png" alt="Jarvis" width="200">
</p>

<h1 align="center">JARVIS</h1>

<p align="center"><b>A personal AI for a Windows PC: it understands rough, typo-filled sentences, does the work, talks back in a dry Tony Stark voice, and asks before it touches anything that matters.</b></p>

> **This is a showcase. The source code is private, and every piece of data you see is demo data.** Nothing here comes from a real inbox, calendar, contact list or file.

## Watch it

[![Watch the tour](screenshots/03-the-workshop.png)](video/jarvis-tour.mp4)

**A 7-minute tour** of the real app running on demo data, narrated by Jarvis in his own voice. Click the picture to play it.

- [**The journey**](docs/JOURNEY.md): how a notes folder became a PC assistant with a face, mistakes included
- [**Every feature**](docs/FEATURES.md): screen by screen, with what works, what is new and what does not exist yet

## Screenshots

<table>
<tr><td width="50%" valign="top"><img src="screenshots/01-meet-the-orb.png" alt="Meet the orb: it forms on a wake, and the cards show what you said and what Jarvis says"><br><b>Meet the orb: it forms on a wake, and the cards show what you said and what Jarvis says</b></td><td width="50%" valign="top"><img src="screenshots/02-speaks-first.png" alt="It speaks first: a mail waiting three days, said once, never nagging"><br><b>It speaks first: a mail waiting three days, said once, never nagging</b></td></tr>
<tr><td width="50%" valign="top"><img src="screenshots/03-the-workshop.png" alt="The Workshop: a living background, a centrepiece and six glass tiles"><br><b>The Workshop: a living background, a centrepiece and six glass tiles</b></td><td width="50%" valign="top"><img src="screenshots/04-map-tile.png" alt="The map tile, enlarged: a wire globe on live public data"><br><b>The map tile, enlarged: a wire globe on live public data</b></td></tr>
<tr><td width="50%" valign="top"><img src="screenshots/05-system-tile.png" alt="The system tile: your machine as a living anatomy (demo numbers)"><br><b>The system tile: your machine as a living anatomy (demo numbers)</b></td><td width="50%" valign="top"><img src="screenshots/06-activity-tile.png" alt="The activity tile: the day by project, from an on-PC log"><br><b>The activity tile: the day by project, from an on-PC log</b></td></tr>
<tr><td width="50%" valign="top"><img src="screenshots/07-projects-tile.png" alt="The projects tile: where you left off, files changed, hours worked"><br><b>The projects tile: where you left off, files changed, hours worked</b></td><td width="50%" valign="top"><img src="screenshots/08-inbox-tile.png" alt="The inbox tile: a reply queue built from made-up mail"><br><b>The inbox tile: a reply queue built from made-up mail</b></td></tr>
<tr><td width="50%" valign="top"><img src="screenshots/09-calendar-tile.png" alt="The calendar tile: free windows and clashes across a made-up week"><br><b>The calendar tile: free windows and clashes across a made-up week</b></td><td width="50%" valign="top"><img src="screenshots/10-recording-mode.png" alt="Recording mode: private text is replaced before it reaches the screen"><br><b>Recording mode: private text is replaced before it reaches the screen</b></td></tr>
<tr><td width="50%" valign="top"><img src="screenshots/11-what-i-look-like.png" alt="The “what do you look like” page: Jarvis's own parts around a live network"><br><b>The “what do you look like” page: Jarvis's own parts around a live network</b></td><td width="50%" valign="top"><img src="screenshots/12-plan-then-yes.png" alt="Create: a plan first, nothing written before you say yes"><br><b>Create: a plan first, nothing written before you say yes</b></td></tr>
<tr><td width="50%" valign="top"><img src="screenshots/13-read-only-mail.png" alt="Mail, read-only: previews on screen, a warning on a message that asks for money"><br><b>Mail, read-only: previews on screen, a warning on a message that asks for money</b></td><td width="50%" valign="top"><img src="screenshots/14-moods.png" alt="A voice with moods: playful when you are, calm and serious when you are stressed"><br><b>A voice with moods: playful when you are, calm and serious when you are stressed</b></td></tr>
</table>

## How it fits together

```mermaid
flowchart LR
  you((You)) --> ears["Ears<br/>hotkey, name, voice"]
  ears --> brain["Brain<br/>understands what you meant"]
  memory[("Notes<br/>personality, rules, memory")] --> brain
  brain --> rules["Rules in code<br/>ask first, read-only, private folder"]
  rules --> hands["Hands<br/>open, create, query, screen, commands"]
  hands --> desk["Desk<br/>activity, vitals, jobs, weather"]
  brain --> voice["Voice<br/>neural and local"]
  hands --> face["Face<br/>orb, Workshop, tiles, pages"]
  voice --> you
  face --> you
```

## Facts

| | |
|---|---|
| Platform | Windows 10 and 11 |
| Built | One small task a day, from 2 October 2026 |
| Automated tests | 1,256, offline, about a minute |
| Modules | 58, one per ability |
| Lines of Python | 12,948 |
| The face | A transparent orb, then the Workshop: 6 glass tiles and 4 pages, all voice-driven |
| Memory | A folder of plain notes you can read and correct |
| Cost | Free tiers only |
| Status | Working. The backend is done; changes are normal work |

---

Copyright (c) 2026 Khushal Vashistha. All rights reserved. Showcase only: the source code is private and no licence is granted.
