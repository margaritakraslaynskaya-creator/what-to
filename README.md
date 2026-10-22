# What to… — Telegram Mini App

One page (`index.html`) that keeps your lists: what to watch, read, buy, see, plus any list you add yourself ("What to cook", "What to try"…). No server and no database: everything is saved in Telegram's own cloud storage for your account, so it syncs between your phone and desktop automatically.

## 1. Put the page online (free, ~5 minutes)

Telegram only opens Mini Apps from an `https://` address. GitHub Pages is the easiest free option:

1. Create a GitHub account if you don't have one, then click **New repository**. Name it e.g. `what-to`, set it to **Public**, create it.
2. Click **Add file → Upload files**, drop in `index.html`, click **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment*, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
4. After a minute the page is live at `https://YOUR-USERNAME.github.io/what-to/`. Open it in a browser to check it loads (in a normal browser it saves to that browser only; that's expected).

Netlify Drop or Vercel work too if you prefer.

## 2. Create the bot and attach the app

In Telegram, open **@BotFather**:

1. Send `/newbot`, choose a display name (e.g. *What to…*) and a username ending in `bot`.
2. Send `/mybots` → pick your bot → **Bot Settings** → **Menu Button** → send your GitHub Pages URL, then a button title like `Open`.
3. Optional but nice: `/mybots` → your bot → **Bot Settings** → **Configure Mini App** → enable it and send the same URL. This adds an **Open** button on the bot's profile and lets you share a direct link `t.me/yourbot?startapp`.

BotFather's menu wording changes from time to time; if a button has moved, look for "Mini App" or "Menu Button" in the bot's settings.

You don't need the bot token for this version, because there's no server. Keep it private anyway.

## 3. Use it

Open the bot and tap **Open**. Tap a list at the top to switch, type at the bottom to add, tap the circle to mark something done, tap an item to add a note or link, move it to another list, or delete it. **+ New list** adds a category; the pencil icon renames or deletes the current one.

## Good to know

- Each Telegram user who opens the bot gets their own separate lists. To share lists with someone, that would need a server (see below).
- Storage capacity is a few megabytes, which is thousands of items.
- To update the app later, upload a new `index.html` to the same repository. Your lists stay, because they live in Telegram, not in the file.

## Possible next step

Sending a message or forwarding a link straight to the bot ("Dune" → added to *watch*) needs a small server with a database, since Telegram's per-app storage is only reachable from inside the Mini App. That can be added later on top of this.
