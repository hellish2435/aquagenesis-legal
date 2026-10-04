# Aquagenesis legal site — how it works

This folder (`Documents\GitHub\aquagenesis-legal`) is its own small
**public** website (GitHub Pages). The game downloads these documents and
shows them in-game, so editing a file here updates the game for everyone
within a few minutes. Your game repository stays private; only this folder
goes public. (It must stay outside the game's folder: GitHub Desktop can't
add a repository that sits inside another one.)

| File | Document | Shown in game as |
| --- | --- | --- |
| `privacy.md` | Privacy Policy | Main menu → Legal, Settings → Legal |
| `terms.md` | Terms of Service | same |
| `ai.md` | AI-Generated Content Disclosure | same |

## One-time setup (about 5 minutes)

1. **GitHub Desktop → File → Add local repository…** → choose this
   `aquagenesis-legal` folder → it says it isn't a Git repository → click the
   **create a repository** link → keep the name `aquagenesis-legal` →
   **Create repository**.
2. **Publish repository** → **untick "Keep this code private"** (Pages needs
   it public on a free account) → Publish.
3. On github.com open the repository → **Settings → Pages** → Source:
   **Deploy from a branch** → Branch **main**, folder **/ (root)** → Save.
   After a minute the site is at `https://<your-github-name>.github.io/aquagenesis-legal/`.
4. Tell Claude your GitHub user name (or put it in
   `data/online_config.gd` → `GITHUB_USER`). That connects the game.

## Editing a document

1. Open the file on github.com (or in any text editor, then commit and push
   with GitHub Desktop) and change the text.
2. **Change the "Last updated" date** at the top (`**Last updated: YYYY-MM-DD**`).
   That date is the document's version: when the Terms or Privacy Policy date
   changes, signed-in players are asked to read and accept the new version.
3. Commit. The website updates in about a minute; the game shows the new text
   the next time a player opens it (allow up to ~5 minutes for GitHub's cache).

## Formatting the game understands

`# Heading`, `## Heading`, `**bold**`, `*italic*`, `- bullet lists`,
`| tables |`, `> notes` and `[link text](url)`. Keep the `---` block with the
`title:` line at the top of each file.

## Before real players use online features

- Replace every **[bracket]** (studio name, contact email, address, governing law).
- Have the Privacy Policy and Terms reviewed by someone qualified.
- Remove the DRAFT notes.
