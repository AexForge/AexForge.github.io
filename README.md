# AexForge — Portfolio Site

A single-page portfolio showcasing Agentic AI / Anthropic / Claude projects.
Plain HTML/CSS/JS — no build step, no dependencies to install.

## What's inside

- `index.html` — the main site (structure, styles, and behavior in one file)
- `career-os.html` — a detailed case-study page for the "AI Career Operating
  System" project (Dify + Groq + Google Workspace architecture), linked from
  the featured project card on the homepage
- Live GitHub repo feed (pulls automatically from `github.com/AexForge`)
- A `featuredProjects` array (inside the `<script>` at the bottom of `index.html`)
  for hand-picking specific projects with your own description — add a
  `caseStudy: "some-page.html"` field to link a project card to its own
  detail page, the way the Career OS project does

## Deploy on GitHub Pages (free)

1. Create a new public repo on GitHub — e.g. `AexForge/AexForge.github.io`
   (using this exact `username.github.io` name makes the site live at the
   root domain; any other repo name works too, just with a `/reponame/` path).
2. Push these files to that repo:
   ```bash
   git init
   git add index.html career-os.html README.md
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/AexForge/AexForge.github.io.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under **Source**, choose the `main` branch and `/ (root)` folder → **Save**.
5. GitHub gives you a live URL in a minute or two:
   - `https://AexForge.github.io` (if you used the `username.github.io` repo name), or
   - `https://AexForge.github.io/your-repo-name/` otherwise.

## Customizing

- **Featured projects:** open `index.html`, find `featuredProjects` near the
  bottom, and add objects like:
  ```js
  {
    title: "Agent Ops Toolkit",
    description: "A short, plain-language description of what it does.",
    tags: ["MCP", "Claude", "Python"],
    repo: "https://github.com/AexForge/your-repo",
    demo: null // or a live URL
  }
  ```
- **Contact email:** replace `hello@example.com` in the Contact section.
- **Bio / skills copy:** edit directly in the `#about` and `#skills` sections.
- **Colors:** all defined as CSS variables at the top of the `<style>` block
  (`--forge`, `--ember`, etc.) — change once, updates everywhere.

## Notes

- The live GitHub feed excludes forks and shows your 6 most recently updated
  public repos. Pin your best work by adding it to `featuredProjects` instead
  of relying on recency.
- This site is intentionally scoped to your technical/professional identity.
  If you later want to add the leadership-coaching side of your work, the
  cleanest path is a separate page (e.g. `coaching.html`) or a second repo —
  keeping the two audiences and tones distinct rather than merging them into
  one page.
