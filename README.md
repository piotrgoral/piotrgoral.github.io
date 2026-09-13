# Blog

Hugo site using the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme (git submodule).

## Prerequisites

```bash
brew install hugo                         # extended edition
git submodule update --init --recursive   # fetch the PaperMod theme
```

## Run locally

From this `blog/` directory:

```bash
hugo server --port 1313
```

Open http://localhost:1313/ — e.g. http://localhost:1313/posts/what-is-a-harness/

The server live-reloads on changes. Add `-D` to include draft posts.

To run it in the background instead:

```bash
nohup hugo server --port 1313 > /tmp/hugo.log 2>&1 &
```

## Stop

- Started in the foreground: press `Ctrl+C` in that terminal.
- Running in the background (or you lost the terminal):

```bash
pkill -f "hugo server"
```

  or find the process by port and kill it:

```bash
lsof -i :1313        # note the PID
kill <PID>
```

## Build

```bash
hugo --minify   # outputs to public/
```
