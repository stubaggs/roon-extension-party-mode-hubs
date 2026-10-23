# Party Hubs for Party Mode

Party Hubs of your own for [Party Mode](https://github.com/stubaggs/roon-extension-party-mode),
the Roon extension that lets guests request music from their phones. Each one is a single
web page that shows what the Party Hub shows (what's playing, up next and played, who
asked for each track, and the code to join) in a design of its own: for a TV, a tablet,
signage or a dashboard.

They need Party Mode 1.4.0 or later, and read what it shares at the addresses under
`/embed/`, described in [EMBED.md](https://github.com/stubaggs/roon-extension-party-mode/blob/beta/EMBED.md).
They're read-only: guests still add tracks on their phones.

## The Hubs

| Page | What it is |
| --- | --- |
| [`party-hub.html`](party-hub.html) | The built-in Party Hub, rebuilt: its layout and styles, with links to join and to download the playlist |
| [`simple-hub.html`](simple-hub.html) | A plainer Hub: what's playing, up next and who asked, with the codes and links to them |
| [`roon-display-hub.html`](roon-display-hub.html) | The Party Hub with Roon's own display page (Roon Display) in place of what's playing: Roon's artist pictures beside the code to join and Up next. Needs the Roon Core's address too. The built-in Party Hub can do this itself (**Party Hub now playing** → **Roon Display**); start here to change it |
| [`qr-codes.html`](qr-codes.html) | Just the codes, with links: to join, and the playlist's once the party ends |

## Using one

1. Download the page (on GitHub: **Download raw file**).
2. Open it in a browser, from disk or from a web server of your own, with the Party
   Hub's address added: `party-hub.html?hub=http://192.0.2.10:8338`. Or open it alone and
   type the address in.

A page has to be opened over `http`, not from an `https` site (GitHub Pages included):
Party Mode speaks plain `http`, and browsers won't let an `https` page reach it. In
Firefox, use a web server rather than opening it from disk, or the covers and codes won't
show.

## Trying other screen shapes

[`ratio-test.html`](ratio-test.html) shows a page in a frame of a common screen shape
(4:3, 16:10, 16:9, 1.85:1, 2:1, 21:9, 2.39:1, 32:9, or the whole window), as large as fits,
with the frame's size and shape at the bottom right. Name the page with `?page=`: one in
the same folder, yours included, or any web address, such as the built-in Party Hub.
Anything else after the `?` is passed on to the page:

- `ratio-test.html?page=party-hub.html&hub=http://192.0.2.10:8338`
- `ratio-test.html?page=http://192.0.2.10:8338/PartyHub`

Opened without `?page=`, it asks for Party Mode's address, with a button for the built-in
Party Hub and one for each page here.

## Adding yours

Made a Hub you like? Add it: see [CONTRIBUTING.md](CONTRIBUTING.md).

## Licence

Copyright © 2026 Stubaggs and contributors. MIT licence (see [LICENSE](LICENSE)): copy,
change and share any of these pages, keeping the notice at the top of the file. The
built-in Party Hub's design comes from Party Mode itself.
