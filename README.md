# Party Hubs for Party Mode

Welcome, Roon Tinkerers!

Your own Party Hub for [Party Mode](https://github.com/stubaggs/roon-extension-party-mode),
the Roon extension that lets guests request music from their phones. Each page here shows
what the Party Hub shows (what's playing, up next, who asked for each track, and the code
to join) in a design of your own, for a TV, a tablet, signage or a dashboard. Tweak an
existing one and make it yours, or start from scratch using
[`example-hub.html`](example-hub.html). Questions and ideas are welcome on
[Party Mode's topic](https://community.roonlabs.com/t/party-mode-extension/325638) on the
Roon forum.

The pages need Party Mode 1.4.0 or later and read what it shares under `/embed/`. They're
read-only: guests still add tracks on their phones. Like the built-in Party Hub, they work
in older TVs' browsers (such as LG's from 2021) and on older iPads.

**How the pages get their data:** every address and field Party Mode shares is in
[EMBED.md](https://github.com/stubaggs/roon-extension-party-mode/blob/beta/EMBED.md), and
[`example-hub.html`](example-hub.html) shows them all in use.

## The pages

These are demos: open them to see what's possible, then copy one as the start of your
own. The first three are copies of the Party Hub that Party Mode already has, rebuilt
from `/embed/`; `example-hub.html` shows every option; the others are simpler starting
points.

| Page | What it is |
| --- | --- |
| [`party-hub.html`](party-hub.html) | **The built-in Party Hub, Standard view.** The code to join down the left; what's playing (cover, title, artist, album and who asked) and Up next on the right. Once the party is over, "Requests are closed" and the code to download the playlist. Party Mode shows the same at `/PartyHub/Standard` |
| [`roon-display-hub.html`](roon-display-hub.html) | **The built-in Party Hub, Roon Display view.** Roon's own Now Playing display (artist pictures, lyrics) on the right, with who asked above it; the code to join and Up next on the left. Needs the Roon Core's address too. Party Mode shows the same at `/PartyHub/Roon` |
| [`basic-hub.html`](basic-hub.html) | **The built-in Party Hub, Basic view.** A plain 16:9 page for TV browsers years behind: the code to join, what's playing and six tracks of Up next, scaled to fit any window. Plain ES5 and CSS, checked back to Chrome 53 and Firefox 47: a starting point for a screen that has to run anywhere. Party Mode shows the same at `/PartyHub/Basic` |
| [`example-hub.html`](example-hub.html) | **Every option, plainly.** Each `/embed/` address and field in a section of its own, with comments: the live stream and its fallback, the status, both codes and links, what's playing (all three cover sizes and the moving position), Up next with the reason it's empty, Played with skips, and Roon Display (framed from your Roon Core's address). Not for a TV: a page to read and copy from |
| [`simple-hub.html`](simple-hub.html) | **A plainer Hub.** What's playing, Up next and who asked for each track, with the code to join, in simple cards: a small page to read and change |
| [`qr-codes.html`](qr-codes.html) | **Just the codes.** The code to join, and the playlist's once the party ends, each with its link: for a printed sign or a second screen |

## Using one

1. Download the page (on GitHub: **Download raw file**).
2. Open it in a browser with your Party Mode address added:
   `party-hub.html?hub=http://192.0.2.10:8338`. Or open it alone and type it in.

On a web server of your own (for example, your existing NAS), put your Party Mode address
in `HUB` (and your Roon Core's in `ROON`, for `roon-display-hub.html`), in the "Your
addresses" block near the top of the page, and it needs nothing added. `hub=` and `roon=`
in the page's address will override.

Open pages over `http`, not from an `https` site such as GitHub Pages: Party Mode speaks
plain `http`, and browsers won't let an `https` page reach it. In Firefox, use a web
server rather than opening the file from disk, or the covers and codes won't show.

## Trying other screen shapes

[`ratio-test.html`](ratio-test.html) shows a page at a common screen shape (4:3 to 32:9,
or the whole window), as large as fits. Name the page with `?page=`: one in this folder,
yours included, or any address, such as the built-in Party Hub. Anything else after the
`?` is passed on:

- `ratio-test.html?page=party-hub.html&hub=http://192.0.2.10:8338`
- `ratio-test.html?page=http://192.0.2.10:8338/PartyHub`

Opened alone, it asks for your addresses and offers every page here. `HUB` and `ROON` work
as above.

## Share yours

Made a Party Hub you're proud of? Please share it: add it here for others to use (see
[CONTRIBUTING.md](CONTRIBUTING.md)), and announce it on
[Party Mode's topic](https://community.roonlabs.com/t/party-mode-extension/325638) on the
Roon forum, with a screenshot.

## Licence

Copyright © 2026 Stubaggs and contributors. MIT licence (see [LICENSE](LICENSE)): copy,
change and share these pages, keeping the notice at the top of each file.
