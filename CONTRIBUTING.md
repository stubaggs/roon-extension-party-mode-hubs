# Adding a Party Hub

Thanks for sharing yours. Open a pull request that adds:

- **`<name>.html`**: your Hub, as one page.
- **`screenshots/<name>.png`**: what it looks like during a party (a made-up one is fine).
- **A line** in the README's table: the file, and what it is in a sentence.

## The guidelines

So that anyone can pick up a Hub and run it at their party, every Hub:

- **Is one self-contained file.** Its styles, scripts and images are in the page. No
  scripts, fonts, styles or images from elsewhere (no CDN), and no requests to anywhere
  but the host's Party Mode address: it works without the internet, and anyone can check
  it by reading one file. The one exception is Roon's own display page, framed, from the
  Core's address the host gives (as `roon-display-hub.html` does, with `?roon=`).
- **Is read-only.** It uses only the addresses under `/embed/` described in
  [EMBED.md](https://github.com/stubaggs/roon-extension-party-mode/blob/beta/EMBED.md),
  never `/api/…`, which can change at any release.
- **Takes the host's Party Mode address** from `?hub=` in its own address, or from `HUB`
  in a "Your addresses" block at the top of the page, and asks for it if neither is
  there, as the pages here do.
- **Starts with the MIT notice** from the top of the other pages, with your name added
  to the copyright line if you like (`Copyright (c) 2026 Stubaggs and contributors, Your
  Name`). By sending a pull request, you agree to your Hub being shared under the MIT
  licence.

## Good to know

- Follow `/embed/events` (a live stream) rather than fetching the files many times a
  second: Party Mode limits the requests each device can make. EMBED.md's "Building a
  page" has the rest.
- Say **tracks**, not songs: a track may be a poem or a speech.
- Use `192.0.2.10` (an address kept for examples) in any example address, never your own.
- Check your Hub in more than one browser, and on the screen you made it for. To see it
  at other screen shapes, put it beside `ratio-test.html` and open
  `ratio-test.html?page=<name>.html&hub=…`.

Every pull request is read before it's merged, and a Hub that doesn't follow a guideline
is sent back with what to change.
