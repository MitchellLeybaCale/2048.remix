# 2048 Remix

A 2048-style game with custom pictures instead of numbers. Use the arrow keys
(or WASD, or swipe on a phone) to slide tiles. Two matching pictures merge into
the next picture in the ranking. Reach the final picture to win — then keep
going if you want.

## Get it online (GitHub Pages)

1. Go to [github.com/new](https://github.com/new) and create a repository
   (e.g. `2048-remix`). Make it **Public** and click **Create repository**.
2. On the new repo page, click **uploading an existing file** and drag in
   everything in this folder (`index.html`, `README.md`, and the `images`
   folder). Commit the changes.
3. Go to **Settings → Pages**. Under "Build and deployment", set **Source**
   to *Deploy from a branch*, pick the **main** branch and **/ (root)**
   folder, then **Save**.
4. After a minute or two, your game is live at:

   `https://YOUR-USERNAME.github.io/2048-remix/`

   That's the link you send to friends. Any time you edit a file in the repo,
   the site updates automatically.

## Add your pictures

Drop your images into the `images/` folder with these exact names, lowest
rank to highest:

| File         | Rank | Default       |
|--------------|------|---------------|
| `tile-1.png` | 1    | Sunshine      |
| `tile-2.png` | 2    | Puppy         |
| `tile-3.png` | 3    | Duomo         |
| `tile-4.png` | 4    | Flatirons     |
| `tile-5.png` | 5    | Knicks        |
| `tile-6.png` | 6    | Beach day     |
| `tile-7.png` | 7    | Spicy marg... |
| `tile-8.png` | 8    | Cup of tea    |
| `tile-9.png` | 9    | Ski day       |

Square images look best (they're shown on a white card, so transparent or
white backgrounds work great). JPGs are fine too — just update the filename
in the config. **If an image is missing, the game shows an emoji + name
instead**, so it's playable before you've added any pictures.

## Customize the ranking

Open `index.html` and find the `TILES` list near the top of the
`<script>` section:

```js
const TILES = [
  { name: 'Sunshine', emoji: '☀️', img: 'images/tile-1.png' },
  ...
];
```

- **Reorder** entries to change the ranking.
- **Rename** the `name` field to change the labels.
- **Add or remove** entries to make the game longer or shorter — the win
  condition is always the last entry in the list. (Classic 2048 has 11
  levels; this version has 9, so it's a bit quicker to beat.)

## Customize the look

All colors live in the `:root` block at the top of the `<style>` section —
change the background, board, and button colors there and everything updates.
