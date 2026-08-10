# Türkiye 2027 — Site

**One page.** `index.html` is the whole thing: interactive checklist, cost, flights, hotels, day-by-day, sights, food, nightlife, Cappadocia, transport, entry and laws. Sticky nav at the top jumps between sections.

Every number now lives in exactly one place. That's what fixes the inconsistency — before, the same figure existed in four files and only some got updated.

---

## The checklist — how it works

**17 dated tasks** from "decide if you're going" (30 August 2026) through "wheels up" (20 May 2027).

- **Add people** with the box at the top. Each person is marked **In / Maybe / Out**.
- **Per-person tasks** (passport, PTO, flights, insurance) show a chip for every person who isn't marked Out. Tap a chip to tick that person off.
- **Group tasks** (book the hotel, book the balloon) have a single Done button.
- **Anyone marked Out is excluded** from the per-person counts automatically.
- Progress bar and a "next up" line track where the group actually is.

### Important: how sharing works

Ticks are saved in **your browser only** — a static site has no database. To share:

1. Click **Share / sync**
2. **Copy code** → paste it into the group chat
3. Anyone else pastes it into their box and clicks **Load pasted code**

There's also **Copy summary for group chat**, which produces a clean who's-in / what's-next message.

**Simplest approach:** one person is the keeper. They hold the real state and post the summary when it changes.

**If you want real multi-user sync**, that needs a backend — Firebase or Supabase, both free at this size. Say the word and I'll wire it up.

---

## Files

| File | What |
|---|---|
| `index.html` | **The site.** The only file that matters. |
| `brief.html` `itinerary.html` `guide.html` `budget.html` `compare.html` | Redirects to `index.html`, so old links you already sent still work |

---

## Delete these — no longer used

```
four-guys-trip-plan.html
thailand-14-day-and-headtohead.html
MASTER-trip-plan.html
COST-SHEET-october.html
WHAT-YOU-ACTUALLY-DO.html
THE-PITCH.html
MAY-2027-RESET.html
AOE4-FACTIONS-AND-DESTINATIONS.html
CIV-HOMELANDS-AS-DESTINATIONS.html
```

Once you're sure nobody's using the old links, the five redirect files can go too.

---

## Deploy / update

**Already live:** upload `index.html`, replace the old one, commit. Live in under a minute.

**First time:** github.com → **+** → **New repository** → `turkey-2027` → **Public** → Create. Click **uploading an existing file**, drag `index.html` and the five redirects in, **Commit changes**. Then **Settings** → **Pages** → Source **Deploy from a branch** → branch **main**, folder **/ (root)** → **Save**. URL appears in a minute:

```
https://YOUR-USERNAME.github.io/turkey-2027/
```

**Editing later:** open the repo → click `index.html` → pencil icon → Ctrl+F to the text → type over it → **Commit changes**.

To add or change a checklist task, find the `TASKS` array near the bottom of `index.html`. Each entry is one line:

```js
{id:'unique', by:'2027-01-31', t:'Task name', per:true, n:'Description.'}
```

`per:true` = every person gets their own tick. `per:false` = one group checkbox.

---

## Two notes

**Public repo means public site.** Nothing here is sensitive — no passport numbers, no booking references. Keep it that way.

**If you change a price, search the whole file for that number first.** The cost table, the tier cards, the top stats and the pitch block all have to agree.
