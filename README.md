# study://lab

A single hub page linking to nine small, single-file, dependency-free visualizers — each one takes a CS concept that's usually taught with static diagrams and makes it interactive.

**[View it live →](#)** *(update this link once GitHub Pages is enabled — see below)*

## What's inside

| Page | Covers |
|---|---|
| `pathfinding.html` | BFS, DFS, Dijkstra &amp; A* racing across a grid you draw walls on |
| `searching.html` | Linear vs. binary search, step by step, side by side |
| `data-structures.html` | Stack, queue, linked list &amp; binary tree — push, pop, insert, live |
| `recursion.html` | The call stack for fibonacci, plus N-Queens backtracking |
| `graph-algorithms.html` | Dijkstra's shortest path &amp; Kruskal's MST on a node-edge graph |
| `hashtable.html` | Buckets, hash collisions, chaining &amp; live resizing |
| `regex.html` | Step through a pattern matching a string, character by character |
| `dp.html` | Memoization tables filling in live: fibonacci, knapsack, edit distance |
| `bitwise.html` | AND / OR / XOR / shifts, one bit at a time, on an 8-bit grid |

`index.html` is the hub — a terminal-styled directory listing that links out to each page above.

No frameworks, no build step, no dependencies other than Google Fonts. Every page is its own self-contained HTML file with its `<style>` and `<script>` inline, same approach as [big-o-explained](https://github.com/tuongphantrue/big-o-explained) and [sorting-algorithms](https://github.com/tuongphantrue/sorting-algorithms).

## Running it locally

Just open `index.html` in a browser — no server or install required. Every link on the hub is a relative path to another file in the same folder, so the whole thing works straight off disk.

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, choose the branch you pushed to (usually `main`) and the `/ (root)` folder.
4. Save. Your page will be live at:

```
https://<your-username>.github.io/<repo-name>/
```

## Adding another topic

1. Copy any existing page as a starting template — they all share the same color/type tokens at the top of the `<style>` block (`--bg`, `--panel`, `--accent`, `--accent2`, `--mono`, etc.) so a new page will look consistent for free.
2. Build the visualization in the `<script>` block — most pages follow the same shape: render initial state, run an algorithm step by step with `await sleep(ms)` between steps, update the DOM after each step.
3. Add a row for it in `index.html`'s listing, linking to the new file.

## License

Feel free to use, modify, and share.
