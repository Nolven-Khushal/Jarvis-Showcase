# Jarvis: every feature

A personal AI for a Windows PC. It understands rough, typo-filled, several-things-at-once sentences (English, Hindi, Hinglish), does the work, talks back in a dry Tony Stark voice, and asks before it touches anything that matters.

Status words used below:

- **Works**: built and tested.
- **New**: built and tested in code, not yet used on the owner's own PC for a full day.
- **Not yet**: does not exist. Listed so nobody is surprised.

All screenshots and the video use **demo data**. See [JOURNEY.md](JOURNEY.md) for how each part came to be.

---

## 1. Talking

- **Ask anything.** General questions, explanations, drafts, jokes. **Works**
- **A personality you can edit.** Jarvis's voice, rules, moods, slang and movie nods live in plain notes in an Obsidian vault, not in code, so the same engine can wear a different persona later. **Works**
- **Mood awareness.** Five moods (playful, neutral, focused, stressed, low), read fresh from every message and never announced. Sarcasm switches off for errors, money, health, family and work trouble. One soft check-in per chat at most. "Chill mode", "stop joking", "focus mode" and "roast me" are obeyed over its own reading. **Works**
- **Slang and movie nods, sparingly.** At most one term per reply, only when the mood allows, delivered deadpan. Never an invented quote. **Works**
- **Honest by rule.** It never claims to have done something it did not do, never invents a person, meeting, number or deadline, never pretends to see the screen. A code-level filter rewrites a reply that breaks a rule before it is shown. **Works**
- **Memory that you can read and correct.** After every chat it writes a short summary note; lasting facts are copied into a "learned" note that it always reads; mood hints go in a mood log. Delete a line in Obsidian to correct it. Nothing ends up in a cloud memory. **Works**
- **Knows what you are doing.** "What's up", "what was I working on yesterday", answered from its own activity log (program names, no keystrokes, no window contents). **Works**

## 2. Hearing and speaking

- **Four ways to wake it.** The hotkey (Ctrl+Alt+J), saying "Jarvis", a wake phrase, or (optional) a double clap. **Works**
- **Three states.** Asleep and listening only for its name, mic off, shut down. A hotkey press brings it back from any of them. **Works**
- **Local ears.** Speech recognition on the PC itself. An optional fast cloud ear can be switched on and falls back to local at any trouble. **Works**
- **A neural voice with a safety net.** The character voice plays when available, with its own daily allowance that warns at 90 percent and falls back to the plain Windows voice at 100. Private text (mail, calendar, screen text) is always spoken by the local voice and never leaves the PC. **Works**
- **Speed work.** A "heard you" chime fills the gap, a short answer starts speaking in about 1 to 2 seconds, the careful second recognition pass only runs when the first is unsure. **Works**
- **Not yet:** "only my voice" speaker check; a phone version.

## 3. Opening things

- **Apps, sites, videos, searches.** "Open Spotify", "play something calm on YouTube", "open the first episode of that series". Opening is allowed the moment you ask; it tells you exactly what it opened and the address. Say "wrong" and it shows the results instead. **Works**
- **Programs on your PC.** Reads the Start Menu list, opens the real desktop app, asks "which one?" when several fit. Games open through Steam when you own them there. **Works**
- **Saved links.** "Remember my university portal is https://…". Banks, payments and logins are never opened from a search guess, only from a link you saved yourself. **Works**
- **Several things in one sentence.** Up to five steps, done in order, one numbered reply; a failing step never stops the others. **Works**
- **Understands how you actually type.** Typos, Hinglish, self-corrections ("no wait, Netflix"), scheduling words (not run), pasted text after "summarise this" (never treated as commands). **Works**

## 4. Making, changing and asking about files

- **Create.** "Create a restaurant database in SQL with dummy data": it shows a plan (folder, every file, one line each), you say yes once, it writes new files only into one workspace folder and opens them in the editor. **Works**
- **Build a database.** A second yes builds a real SQLite database from the SQL files, in a locked-down sandbox with size and time caps. If the build fails it offers a fix as a before-and-after diff and retries once. **Works**
- **Ask the data.** "How many menu items, and the average price?" It writes one read-only query, shows it, and every number comes from the database, never from the AI. **Works**
- **Export.** Every table to a new Excel workbook, or CSV folders to a workbook. Values only, nothing can become a formula, never overwrites. **Works**
- **Edit.** Shows the exact change as a diff, asks yes, keeps a backup of the old file. **Works**
- **Delete.** Moves to a trash folder after a yes. Nothing is ever erased. **Works**
- **Open and list.** "Open that Excel", "open that folder", "show my projects". Text and code open as text, never run. **Works**

## 5. Mail, calendar, WhatsApp, YouTube (read-only)

- **Gmail, two accounts.** "Check my mail", "any important mails", "find email about the audit", "emails from Alex". Sender, subject and a short preview only, shown on screen, never sent to the AI. Mails asking for payment or credentials get a warning mark. **Works**
- **Calendar.** Today and the week, read-only. **Works**
- **WhatsApp.** The unread count from Windows notifications (no unofficial tools, no ban risk). **Works**
- **YouTube.** New uploads from the channels you follow, no key needed. **Works**
- **Speaks first.** While the PC is on it tells you when something new matters: a VIP's mail, a meeting in ten minutes, a favourite channel's upload. Each thing is said once, not at start-up, never in quiet hours or focus mode, at most six interruptions an hour, and what was held back comes out afterwards as one short digest. No AI request is used. **Works**
- **Open-loop nudges.** "Alex wrote to you three days ago and you haven't replied. Missed it, or leaving it?" Once at two days, once at seven, never again. "Who is waiting on me?" lists them. **Works**
- **Focus controls.** "Focus mode", "quiet for 30 minutes", "what did I miss". **Works**
- **Cannot send mail or messages.** **Not yet**

## 6. The morning routine

The first wake of the morning offers "Shall I run your morning routine?". On yes: a greeting that is never the same twice, the mail and WhatsApp counts, new YouTube uploads, the work apps opened in order, and the wake-up song. No AI request is used. **Works**

## 7. Seeing and using the screen

- **Read the screen (on request).** Reads the text of one window with Windows' own offline reader; asks before sending any of it to the AI. Refuses banking, password and private-browsing windows and anything in the off-limits folder. **Works**
- **What can I click.** Lists the buttons, tabs and links of the window in front. **New**
- **Use the screen.** "Click save", "type hello world", "press enter", "scroll down", "switch to Chrome". Uses Windows accessibility so the mouse does not move. Asks yes first for send, delete, pay, install, agree, log out. Never types into password or card fields. **New**
- **Run a command.** "Run git status", "use the terminal to count the lines in notes.md". One command, shown first, validated against an allow-list, run inside the workspace folder only, 30 seconds, never as admin, never deleting, installing, downloading or touching settings. **New**
- **Cannot see pictures, games or charts** (text only). **Not yet**

## 8. Its own browser window

Videos Jarvis plays open in a separate Chrome window with its own profile. It clicks "Skip" when an ad allows it, refreshes (at most four times) when it does not, presses Play if autoplay was blocked, and tells you only if it gives up. It only visits YouTube and the Spotify web player, never logs in, never types. **Works** (Spotify play needs a one-time login by you.)

## 9. The desk

- **Activity log.** Which program is in front and whether you are at the keyboard, kept on the PC only. "What did I do on Tuesday", hours per project. Banking, password and private windows are logged as "Private". **Works**
- **Laptop vitals.** Battery, memory, disk space, graphics-card temperature, internet. One plain warning when something is wrong. **Works**
- **Jobs with an ETA.** Wrap a long task and ask "how's the render?": "62 percent, about four minutes left". **Works**
- **Weather and air quality.** "Will it rain", "air quality". Only the city name leaves the PC. **Works**
- **Wellbeing nudges.** A stand-up reminder after a long stretch, a gentle one-off after midnight. **Works**
- **Project lab.** "Where did I leave off": last change, files changed, hours worked per project. **Works**
- **Protective pause.** If the laptop overheats it can offer to pause a program from a short list, after your yes. It never closes or deletes anything. **Works**
- **Dropped on purpose:** heart rate and health readings (no sensor on the PC).

## 10. The orb and the conversation cards

A transparent, always-on-top orb in the corner of the screen you are on. It forms out of nothing when Jarvis wakes, pulses with his voice, and fades away a few seconds after he goes quiet. Next to it, glass cards show what you said, what Jarvis says (word by word, lists as rows), and heads-ups. Clicks pass straight through; it never takes the keyboard. Mail, calendar and WhatsApp text is replaced by a neutral line in **recording mode**. **Works**

## 11. The Workshop

Say "suit up". A circle opens from the orb and a short film plays (a procedurally built reactor assembling, igniting, settling into a heartbeat), then dissolves into the Workshop. "Stand down" closes it.

- **Living background.** A flowing plasma with a neural constellation, in six palettes. Time of day picks a pair; every suit-up takes the other of the pair; "next theme", "lock this one", "unlock". It reacts to Jarvis's state and voice level. **Works**
- **The centrepiece.** Two interlocking Möbius rings built from about 300 chrome scales each around a tiny black hole, lit by a procedural photo studio. **Works**
- **Six glass tiles, three each side, tilted toward the core.** Everything is voice-driven: "enlarge the map", "close it", "next tile".
  - **Map:** a wire-frame globe on live public data (earthquakes, city weather, the space station), dive into any place over 3D buildings, a smooth tour, an automatic quality governor. **Works**
  - **System:** a pulse orb driven by CPU load plus four liquid inner tiles (processor, memory tank, drive, network); expanded, an "anatomy" of the machine and a treemap of programs by memory and CPU. **Works**
  - **Activity:** today as a clock strip coloured by project, focus blocks, the last 14 days. **Works**
  - **Projects:** "where you left off", candlesticks of files changed, hours worked, a 14-day heatmap. **Works**
  - **Inbox and Calendar:** reply queue, week view with free windows and clashes. Show "not connected" until you sign in. **Works** (needs your sign-in)
- **Voice pill.** A smoke-shader bar at the bottom: smoke grows from the middle with the loudness of your voice or his. **Works**
- **Work mode.** "Let me work": the Workshop steps out of the way so you can use your programs. **Works**
- **Pages over the wall:**
  - **What do you look like:** a map of Jarvis's own parts (senses, hands, face, brain) around a live neural-network visual, with real numbers. **Works**
  - **Show gestures:** your hands through the camera as skeletons, ten gestures, four control panels. **Read-only on purpose:** it never presses or moves anything. **Works in code; not tried with a real hand**
  - **Show the team:** a 3D office of the outreach agents. **Mock-up with sample numbers; not wired to real work**
  - **Suit status:** a diagnostic of Jarvis's own systems. **Works**

## 12. Safety and privacy, by design

- **Ask first** for sending, deleting, paying, posting, installing and starting something unasked. Enforced in code, not only written down.
- **Private folder** never read and never sent anywhere; an off-limits list of folders that apps in them are never opened from.
- **Anything read from mail, web or files is data, never instructions.** A pasted "ignore your rules" does nothing.
- **Read-only wherever it can be:** mail, calendar and the database questions use read-only access, so even a bug cannot change anything.
- **Cost guards:** daily caps on AI requests, tokens and voice characters, checked before each call and failing closed.
- **One-way window.** The face only listens to the brain; nothing on screen can make Jarvis do anything. The control channel accepts one thing (wake) and only from the PC itself.
- **Recording mode** hides private text from the screen.
- **Tests:** 1,256 automated tests, offline, run in about a minute.

## 13. What it cannot do

Send mail or messages, spend money, make calls, run unlimited commands (the top tier does not exist on purpose), see pictures, or know who is speaking.
