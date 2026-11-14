# System Design Storybook

Learn system design for big-tech interviews as if you were 5 years old. Each topic starts as a short kids' story, then gives the real engineering version, the trade-offs, a line you can say in the interview, and a quiz question.

**Live app:** https://juhiajmera.github.io/system-design-podcast/

## Features

- **Read mode:** a story, an architecture diagram, the grown-up explanation, key points and a quiz for every topic.
- **Podcast mode:** two hosts talk through each episode. Maya is the engineer and Leo is preparing for interviews. It uses your device's built-in voices, with speed control, a choice of voice for each host, autoplay, and a transcript that follows along.
- **Quiz mode:** every question in random order, with a score at the end.
- **Progress tracking:** mark topics as understood. Progress is saved in your browser.
- Works on desktop and phone, in light and dark mode.

## What's covered (43 episodes)

**22 core concepts**

| Chapter | Topics |
|---|---|
| Start here | How to answer a design question · Back-of-the-envelope math |
| Getting to the server | DNS · CDN · Load balancer · API gateway · Polling, long polling & WebSockets |
| Storing data | SQL vs NoSQL · Database indexes · Replication · Sharding · Consistent hashing · CAP theorem |
| Making it fast | Caching · Bloom filter |
| Reliability | Message queues · Rate limiting · Idempotency & retries · Unique ID generation · Monolith vs microservices · Consensus & leader election · Batch vs stream processing |

**21 classic interview questions**, each worked through as requirements, estimates, components and deep dives

| Area | Questions |
|---|---|
| Core web products | URL shortener · News feed · Photo sharing app · Search autocomplete · Notification system |
| Real-time | Chat app · Collaborative document editor · Ride-hailing app · Gaming leaderboard |
| Media & storage | Video streaming platform · Cloud file storage |
| Money & correctness | Payment system · Ticket booking system |
| Data at scale | Web crawler · Top-K trending · Metrics & monitoring system · Nearby places |
| Infrastructure | Distributed key-value store · Distributed cache · Distributed message queue · Distributed job scheduler |

## How to run it

The whole app is one file, `index.html`, with no build step, no server and no dependencies.

- **On a computer:** double-click `index.html` to open it in Chrome, Edge, Safari or Firefox.
- **On a phone:** open the live link above, then use **Add to Home Screen** to open it like an app.

## Hosting on GitHub Pages

1. Push `index.html` to a public repository.
2. Go to **Settings → Pages**, choose **Deploy from a branch**, then pick `main` and `/ (root)`.
3. After a minute or two the site is live at `https://<your-username>.github.io/<repo-name>/`.

## Notes

- **Voices:** the podcast uses the browser's built-in text-to-speech, so voices differ by device. Microsoft Edge on Windows and Safari on iPhone usually sound the most natural.
- **Phones:** most phones stop the browser's speech when the screen locks, so keep the screen on while listening.
- **Offline:** the app works without internet, but it falls back to system fonts.
- **Saved data:** progress and podcast settings are stored in your browser only. They aren't synced between devices.

## Adding a topic

Topics live in the `TOPICS` array inside `index.html`. Copy an existing entry and edit its fields:

| Field | What it holds |
|---|---|
| `id` | A unique short name, also used in the page link |
| `group` | The chapter the topic appears under |
| `title`, `tag` | The topic name and a one-line hook |
| `eli5` | The kids' story |
| `real` | The grown-up explanation |
| `flow` | The diagram steps. A nested array shows parallel boxes |
| `points` | The key points or design steps (simple HTML is allowed) |
| `say` | A sample line to use in the interview |
| `q`, `opts`, `a`, `why` | The quiz question, the options, the index of the correct option (counting from 0) and the explanation |
| `kind: "design"` | Optional. Marks a full interview question, which changes the headings and podcast script |

The podcast script for each episode is generated from these fields, so a new topic gets its own episode automatically.

## Credits

The explanations are original and cover standard system design topics. Use the app alongside books, courses and real practice.
