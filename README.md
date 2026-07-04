# Linux Basics Lab — Case 4111 (Zeroday Academy)

A single, self-contained simulated terminal for the Linux demo. Boots inside `~/case-files`; the student runs `ls` then `grep -r "4111" .` to find a stolen card number hidden in one of 10,000 files. `cd ..` opens a five-command practice sandbox (`pwd`, `ls`, `cd`, `cat`, `grep`, plus tab-completion, history, a hidden `.secret`, and a CTF flag). No build step, no backend, no dependencies.

## Files
- `index.html` — the whole lab (HTML + CSS + JS inline)
- `.nojekyll` — tells GitHub Pages to serve files as-is (skip the Jekyll build)

## Deploy to GitHub Pages
1. Create a repository and put `index.html` and `.nojekyll` at the **root**.
2. Push to the `main` branch.
3. **Settings → Pages → Build and deployment.**
4. Source: **Deploy from a branch** · Branch: **main** · Folder: **/ (root)** · **Save**.
5. Live in ~1 minute at `https://<username>.github.io/<repo>/`.

### Hosting both demos in one repo
If you want the HTTP demo and this lab on the same GitHub Pages site, use subfolders:
```
/
  .nojekyll
  http/index.html     (the HTTP vs HTTPS demo)
  linux/index.html    (this lab)
```
They'll live at `…github.io/<repo>/http/` and `…github.io/<repo>/linux/`. One `.nojekyll` at the root covers the whole site.

## Notes
- Works at a user site (`<username>.github.io`) or a project subpath — there are no relative asset paths to break.
- Everything runs client-side; it's a *simulated* shell (safe, offline, no real filesystem), which is exactly why it works on static hosting.
