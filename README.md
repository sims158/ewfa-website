# EWFA site — deploy

`index.html` is a single self-contained file: images, flags, logos and fonts are inlined. Nothing else needs uploading.

## Option A — plain upload
Upload `index.html` into `public_html` via cPanel File Manager or FTP.

## Option B — cPanel Git
1. Push this folder's contents to a GitHub repo. The repo root must contain `index.html` and `.cpanel.yml`.
2. Edit `.cpanel.yml`, replacing `USERNAME` with your cPanel username. The correct server path is shown on the cPanel dashboard as the home directory, e.g. `/home/ewfaorg/public_html`.
3. cPanel → Git Version Control → Create → Clone a Repository. Repository path: `repos/ewfa` (outside `public_html`).
4. After each push: Manage → Update from Remote, then Deploy HEAD Commit.

Private repo: cPanel → SSH Access → Manage SSH Keys → generate and authorize a key, add the public key to the GitHub repo as a Deploy key, then clone using the SSH URL (`git@github.com:owner/repo.git`).

## Re-exporting
Each new export from the design replaces `index.html`. Commit and redeploy.
