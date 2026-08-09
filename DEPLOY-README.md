# Türkiye 2027 — How To Put This Online

A static website. No build step, no dependencies, no code. Just HTML files that GitHub will serve for free at a public URL you can text to the group.

**Time to deploy: about five minutes.**

---

## Step 1 — Rename five files

GitHub Pages needs the landing page to be called `index.html`, and the links inside it point to specific filenames. Put these five files in one folder on your desktop and rename them exactly like this:

| Current filename | Rename to |
|---|---|
| `index.html` | `index.html` *(already correct — don't touch it)* |
| `TURKEY-MASTER-BRIEF.html` | `brief.html` |
| `TURKEY-FINAL-PLAN.html` | `itinerary.html` |
| `TURKEY-THE-BOOK.html` | `guide.html` |
| `FOUR-WAY-COMPARISON.html` | `compare.html` |

Case matters. All lowercase, exactly as written.

---

## Step 2 — Make the repository

1. Go to **github.com** and sign in. Make a free account if you don't have one.
2. Click the **+** in the top right → **New repository**.
3. Name it something like `turkey-2027`.
4. Set it to **Public**. *(GitHub Pages requires public on free accounts.)*
5. Leave every checkbox unticked. Click **Create repository**.

---

## Step 3 — Upload the files

1. On the new empty repo page, click **uploading an existing file**.
2. Drag all five renamed HTML files in at once.
3. Click **Commit changes**.

---

## Step 4 — Turn on Pages

1. In the repo, click **Settings** (top bar).
2. Click **Pages** in the left sidebar.
3. Under **Source**, choose **Deploy from a branch**.
4. Branch: **main**. Folder: **/ (root)**. Click **Save**.
5. Wait one to two minutes, then refresh the page.

Your URL appears at the top:

```
https://YOUR-USERNAME.github.io/turkey-2027/
```

That's the link you send to the group. It works on phones.

---

## How to update it later

Say a price changes or you lock in a hotel.

1. Open the repo on github.com.
2. Click the file you want to change — for example `brief.html`.
3. Click the **pencil icon** (Edit this file).
4. Use **Ctrl+F** / **Cmd+F** to find the text you want to change and type over it.
5. Scroll down, click **Commit changes**.

The live site updates in under a minute. No rebuild, no deploy step.

**Easier option:** just tell me what changed and I'll regenerate the file. Then you re-upload it — GitHub asks if you want to replace the existing one, and you say yes.

---

## Adding a new page later

1. Upload the new HTML file to the repo.
2. Edit `index.html` and copy one of the existing `<a class="doc ...">` blocks, changing the `href`, the title, and the description.

---

## Two things worth knowing

**Anyone with the link can see it.** A public GitHub repo is public. Nothing here is sensitive — no passport numbers, no card details, no booking references — so it's fine. **Keep it that way.** Don't put confirmation numbers or personal details in these files.

**You can add a custom domain.** If you want something like `turkey2027.com` instead of the github.io URL, buy the domain (~$12/year) and point it at the repo under Settings → Pages → Custom domain.

---

## If GitHub feels like too much

**Netlify Drop** is the lazy alternative: go to `app.netlify.com/drop`, drag the whole folder onto the page, and you get a live URL in about ten seconds with no account needed. The tradeoff is that updating means re-dragging the whole folder each time, and the URL is a random string unless you sign up.

GitHub is the better call if you're going to be editing this over the next nine months. Netlify is the better call if you just want a link in the group chat tonight.
