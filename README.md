# Chatdown

**Turn your Google AI Mode chats into clean Markdown.**

A tiny, single-file web app that turns a **saved Google AI Mode (Gemini) conversation** into a clean, readable chat — like reading an iMessage thread instead of a cluttered search page.

You save the Google page, drag the `.html` file onto Chatdown, and it rebuilds the whole conversation: your prompts and the AI's answers, properly formatted, with dark mode, and one-click **copy or download as Markdown**.

💡 **Why?** Long AI Mode sessions hold a lot of useful context. Export the whole thing to Markdown and hand it to another model (like Claude) so it can pick up where you left off and build on what you discussed.

> 🔒 **Completely private — your chats never leave your device.** Everything is rendered right in your own browser. Nothing is uploaded, *ever* — no server, no account, no tracking — so **nobody but you ever sees the conversations you open here.** Want to be extra sure? Run it fully offline (see [Private by design](#-private-by-design) below).

<!-- 📺 Demo video: soon -->

---

## How to use it

1. **Have your chat in Google AI Mode.** Use Google Search → AI Mode and ask whatever you like.
2. **Save the page.** Press `Ctrl/Cmd + S` (or right-click → *Save As*) and choose **"Webpage, Complete"**. You'll get an `.html` file (and a folder of assets you can ignore).
3. **Open Chatdown.** Go to the live page: [Chatdown](https://maxsikorski.github.io/chatdown/)
4. **Drag the `.html` file** onto the drop zone (or click **Browse Files**).
5. **Read, theme, and export.** Toggle light/dark with the ☀/🌙 button, then **Copy as Markdown** — or click the **⬇ download** button to save a `.md` file — to take the whole conversation anywhere.

That's it. To view another chat, click **← Back** and drop a new file.

---

## Features

- 🧩 **Works with old *and* new Google AI Mode saves** — the parser pairs each prompt with its own answer structurally, so it survives Google's layout changes. If a page looks like an unrecognized version, it still shows a best-effort view with a small heads-up banner.
- 🌗 **Light & dark mode** (remembers your choice).
- 📋 **Copy *or* download as Markdown** — headings, lists, tables, links, and code blocks preserved. Download saves a `.md` file named after the chat.
- 📱 **Responsive** — works on phone and desktop.
- ⚡ **No dependencies, no build, no server** — just one HTML file.

---

## 🔒 Private by design

Chatdown has no backend, no analytics, and makes **no network requests at all** — every file it needs is inside `index.html`. Your data simply never goes anywhere.

- **Everything happens in your browser.** Your saved page is read and rendered locally, on your own device.
- **Nobody else can see your chats.** What you open in Chatdown is never uploaded, stored, or transmitted — it stays with you.
- **Works fully offline.** Download `index.html` and open it directly — no internet connection required. Turn off your Wi-Fi and it still works exactly the same.
- **No accounts, no tracking, no cookies.** Nothing to sign up for, and nothing watching.

Don't just take our word for it — it's a single, readable file. Open `index.html` and see for yourself.

---

## Run or host it yourself

Because it's a single static file, hosting is trivial:

**Option A — GitHub Pages (recommended)**
1. Fork or create a repo containing `index.html`.
2. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**, pick `main` and `/ (root)`.
3. Your viewer is live at `https://<your-username>.github.io/<repo-name>/`.

**Option B — Just open it locally**
Double-click `index.html`. It works straight from your file system — no install required.

---

## How it works (for the curious)

Everything lives in [`index.html`](index.html) — inline HTML, CSS, and JavaScript, no frameworks.

When you drop a saved page, the app reads the HTML text, finds each user prompt and AI response, pairs them in document order (the answer that follows a prompt belongs to that prompt), strips Google's UI chrome, scripts, and tracking, and re-renders the result as clean chat bubbles. Nothing is fetched or sent anywhere.

---

## License

Released under the [**MIT License**](LICENSE) — free to use, modify, and share.
