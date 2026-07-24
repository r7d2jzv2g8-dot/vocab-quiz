# CNT Exam Prep

Two self-contained study tools built for a CompTIA-style CNT certification: a full practice dashboard covering Fundamentals, Networking, OS, Scripting, and Security, and a separate vocabulary + punctuation quiz. Both are single HTML files — no build step, no dependencies beyond a browser.

## Live tools

- **[CNT Dashboard](./cnt_dashboard.html)** — practice questions across all five exam sections, weak-topic tracking, a custom topic picker, a Pomodoro timer, and an exam-day countdown.
- **[Vocabulary + Punctuation Quiz](./vocab_punctuation_quiz.html)** — 468 words tested on both definition and correct punctuation mark (em dash, colon, semicolon, hyphen), weak-word tracking, a word-of-the-day feature, and three word games: Hangman, Spelling Bee, and a mini crossword.

*(Once hosted, replace the relative links above with your actual GitHub Pages URLs, e.g. `https://yourusername.github.io/repo-name/cnt_dashboard.html`.)*

---

## CNT Dashboard

### What it covers
- **154+ fixed practice questions** across four sections (Networking, OS, Security, Fundamentals), plus **unlimited procedural content** in Scripting (10 code-tracing generators) and Networking (subnetting, and realistic generated `netstat`/`ip route`/`iptables`/`nmap`/`ps aux` output).
- **Weak-spot tracking** at the individual topic level — not just section-wide — with a dedicated card showing exactly which topics need work and one-tap practice for any of them.
- **Custom topic picker** — build a session from any mix of specific topics across any section, not just whole-section or weak-topic practice.
- **Section strength tiles**, a running correct/incorrect tally during each session, and a mid-session exit that doesn't lose progress already made.
- **Pomodoro timer** with configurable focus/break durations, and an exam-day countdown.

### Files it depends on
The dashboard's "Reference materials" section links to these files by relative path — they need to sit in the same folder as `cnt_dashboard.html` for those links to resolve once hosted:

```
cnt_dashboard.html
cnt-manifest.json
cnt-service-worker.js
cnt-icon-192.png
cnt-icon-512.png
diagnostic_exam.html
Final-Exam-Prep-Guide.pdf
Cheat-Sheet-1-Fundamentals-Networking.pdf
Cheat-Sheet-2-Linux-Unix.pdf
Cheat-Sheet-3-Windows.pdf
Cheat-Sheet-4-Scripting.pdf
Cheat-Sheet-5-Security.pdf
Cheat-Sheet-6-Forensics.pdf
```

If any of these are missing, the dashboard itself still works fully — only the reference links under that section will 404. The PWA files (`cnt-manifest.json`, `cnt-service-worker.js`, and the two icon PNGs) are needed specifically for "Add to Home Screen" and offline access to work — the dashboard's core functionality doesn't depend on them.

### Progress data
Section scores, per-topic weak-spot tracking, and Pomodoro settings are all stored in the browser via `localStorage`, scoped to wherever the file is hosted. On GitHub Pages, that means progress persists reliably across visits to the same URL, unlike opening a local file directly, where storage can behave inconsistently depending on how the file was saved or reopened.

---

## Vocabulary + Punctuation Quiz

### What it covers
- 468 words, each testing both **definition recall** and **punctuation judgment** (identifying which of four marks — em dash, colon, semicolon, hyphen — correctly completes a sentence).
- **Weak-word tracking** that treats definition weakness and punctuation weakness as separate signals per word, so practice targets the specific gap rather than re-testing an already-mastered half.
- **Targeted practice by punctuation mark** — drill just semicolons, just hyphens, etc., directly from the progress screen.
- **Three word games**, all built from the same word list: **Hangman** (guess the word from its definition), **Spelling Bee** (find words from a 7-letter set, bonus-highlighted when they're one of your vocab words), and a **mini crossword** (30 puzzles, each a word crossed with several others at real shared letters).
- Word-of-the-day, a practice streak, and voice playback for pronunciation (where the browser supports it).

### Files it depends on
The core quiz works from `vocab_punctuation_quiz.html` alone. These additional files enable "Add to Home Screen" and offline access, the same as the CNT dashboard:

```
vocab_punctuation_quiz.html
vocab-manifest.json
vocab-service-worker.js
vocab-icon-192.png
vocab-icon-512.png
```

### Progress data
Same storage approach as the dashboard above — `localStorage`, scoped per-origin, persists across visits once hosted.

---

## Hosting on GitHub Pages — step by step

This uses GitHub's website only — no command line or git installation needed.

### 1. Create a GitHub account (skip if you already have one)
Go to [github.com](https://github.com) and sign up. It's free.

### 2. Create a new repository
1. Click the **+** icon in the top-right corner → **New repository**.
2. Give it a name, e.g. `cnt-exam-prep` (no spaces — use hyphens).
3. Set it to **Public** (required for free GitHub Pages hosting).
4. Leave everything else at its default, and click **Create repository**.

### 3. Upload the files
1. On your new repository's page, click **Add file → Upload files**.
2. Drag in every file listed in this README under "Files it depends on" for both tools — that means both HTML files, both manifests, both service workers, all four icon PNGs, and the CNT dashboard's cheat sheets/prep guide/diagnostic exam.
3. Scroll down and click **Commit changes**.

*(GitHub's upload page accepts multiple files at once — you don't need to do this one at a time. If you ever need to update a file later, use the same **Add file → Upload files** flow; uploading a file with the same name overwrites the old version.)*

### 4. Turn on GitHub Pages
1. In your repository, click **Settings** (top menu bar).
2. In the left sidebar, click **Pages**.
3. Under "Build and deployment," for **Source**, select **Deploy from a branch**.
4. Under "Branch," select **main** and **/ (root)**, then click **Save**.
5. Wait a minute or two — GitHub will show a message with your live URL once it's ready, in the form:
   `https://yourusername.github.io/cnt-exam-prep/`

### 5. Find your tools
Your two tools are now live at:
- `https://yourusername.github.io/cnt-exam-prep/cnt_dashboard.html`
- `https://yourusername.github.io/cnt-exam-prep/vocab_punctuation_quiz.html`

(Replace `yourusername` and `cnt-exam-prep` with your actual GitHub username and whatever you named the repository.)

### 6. Bookmark them, or add to your phone's home screen
Once live over HTTPS, both support "Add to Home Screen" on mobile for offline access — open the URL in your phone's browser, then use the browser's share/menu button to add it.

---

*No API keys, no backend, no build process — everything in both tools runs entirely in the browser.*
