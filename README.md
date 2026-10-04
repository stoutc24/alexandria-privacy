# Privacy Policy for Alexandria

**Last Updated**: August 27, 2026

## Introduction

Alexandria is a client for media servers **you** run. It has no account
system, no backend of its own, and no analytics. Your library, your
credentials, and your listening history live on your device and on your
servers.

This policy describes exactly what leaves your device, when, and to
whom. Where a feature sends anything to a third party, that is stated
plainly below rather than buried.

---

## What Alexandria Stores On Your Device

- **Server connection details** — the addresses of the media servers you
  add (Audiobookshelf, Kavita, Plex, Jellyfin, Komga, Navidrome,
  Grimmory/BookLore, Calibre, Calibre-Web, Storyteller, Stump, and any
  OPDS catalogue).
- **Credentials** — usernames, passwords, API keys and tokens, held in
  the platform secure store (iOS Keychain, Android
  EncryptedSharedPreferences) and excluded from device backups.
- **Playback and reading progress**, bookmarks, notes and highlights.
- **A local index of your library** (titles, authors, series, genres,
  years, durations, cover URLs) used for search, statistics and
  recommendations.
- **Statistics and reading plans** you create.
- **Downloaded media** you choose to download.
- **AI chat history**, when you use the optional Librarian — the
  conversations are kept on your device so you can return to them, and
  can be deleted at any time from the chat screen.

None of this is transmitted to the developer. Alexandria has no server
that receives your data.

---

## Where Your Data Goes

### 1. Your own servers

The main data flow. Alexandria connects directly to the servers you
configure, using the credentials you provide, to browse, stream,
download, and sync your progress. Nothing passes through us.

### 2. Your own AI server — optional, off by default

If you enable **Settings → AI** and point Alexandria at a model
endpoint, features such as The Librarian, playlist prompts, "catch me
up" recaps, shelf suggestions and describe-a-book send requests to
**the endpoint you configured** — which may be software on your own
machine (Ollama, LM Studio, llama.cpp) or a third-party cloud provider
if you choose one.

What is sent: **media metadata and your own typed messages** — titles,
authors, series and volume numbers, genres, artist and album names,
reading progress, and the text of your questions.

What is never sent: credentials, API keys, tokens, server addresses,
file paths, or cover-image URLs.

If you configure a cloud provider, that provider's own privacy policy
governs what it does with the request. Alexandria ships no API key and
no default endpoint, and this feature stays off until you turn it on.

### 3. Third-party services used by specific features

These receive **content metadata only** — never your credentials, and
never an identifier that ties a request to you personally.

| Service | When | What is sent |
|---|---|---|
| **LRCLib** (lrclib.net) | When lyrics are shown for a track | Track title, artist, album, duration |
| **Last.fm** (audioscrobbler.com) | When building music recommendations | Artist names |
| **Audible catalogue API** (api.audible.com) | Upcoming-releases sync, roughly every 15 days | Author names from your library (up to 15) |
| **Plex.tv** | Only if you sign in to Plex | Plex's own sign-in flow, handled by Plex |
| **RevenueCat** | Subscription purchase and restore | A random app user ID, purchase receipts, and basic device/app info |

### 4. Downloads that carry no personal data

Read-Along speech models are fetched from Hugging Face and from the
project's GitHub releases. These are ordinary file downloads and contain
nothing about you or your library.

---

## What Alexandria Never Does

- No analytics, telemetry, tracking, or advertising SDKs.
- No developer-operated server receives your library, credentials or
  activity.
- Your credentials never leave your device except to authenticate with
  the server they belong to.
- Nothing is sold, rented, or shared for marketing.

---

## Speech, Text and Media Processing

Read-Along transcription runs **entirely on your device** — Apple's
on-device speech engine on iOS, a locally downloaded Whisper model on
Android. Audio is never uploaded for transcription. Translation uses
Apple's on-device translation where available.

---

## Data Retention and Deletion

Everything is on your device, so you control it:

- **Clear All Cache** (Settings → Downloads & Storage) removes local
  data other than credentials.
- **Downloads** can be deleted individually or in bulk from the
  Downloads screen.
- **AI chat history** can be cleared from the Librarian's History sheet.
- **Signing out** removes the credentials for that server.
- **Uninstalling** removes everything Alexandria stored.

We cannot delete your data on request because we never receive it. Data
held by RevenueCat (purchase records) or by an AI provider you chose is
subject to that company's policy.

---

## Children's Privacy

Alexandria is not directed at children under 13 and collects no personal
information from anyone. Content shown comes from servers the user
configures.

---

## Permissions

**Android**: internet and network state; notifications (playback
controls and reminders); foreground service (background playback and
downloads); storage (downloaded files).

**iOS**: background audio; local notifications; network access. Siri and
Spotlight integration where enabled.

---

## Changes to This Policy

Material changes will update the date above and be noted in the app's
release notes. This revision (August 2026) documents the optional AI
feature, local AI chat history, and the third-party services listed in
section 3, which earlier versions of this policy did not describe.

---

## Contact

**Email**: stoutservers@gmail.com

---

## Summary

Alexandria is a client, not a service. Your servers, your credentials,
your library — all local. A small number of well-scoped lookups go to
third parties to power lyrics, recommendations and release dates, and an
AI endpoint receives library metadata **only if you configure one**.
There is no tracking, no advertising, and no server of ours holding
anything about you.

---

**Version**: 2.0 — covers Alexandria 3.1.0
