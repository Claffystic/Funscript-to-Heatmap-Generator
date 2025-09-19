# Funscript-to-Heatmap-Generator
Generates Funscript to Heatmap in Python. 
Vibecoded with Claude, GPT, and Kimi lmao.

Originally made for previewing funscripts in Yazi, but could still be useful for anyone I guess.

### Usage
```bash
python funscript2png <filename>.funscript out.png
```

### Preview
Heatmap:
<img width="1200" height="290" alt="image" src="https://github.com/user-attachments/assets/a9b7ac72-3cf3-4f6d-878b-bd2f9b3e3378" />

In Yazi:
<img width="1919" height="1015" alt="image" src="https://github.com/user-attachments/assets/89916970-7c29-4b07-a93b-3652dcdc8683" />

### Install for Yazi Preview (Linux)
1. `git clone` or download the repo
2. put `funscript2png` to anywhere you can set path (I used `~/.local/bin/`)
3. Drag the file into `~/.config/yazi/plugins` (So full path should look like this: `~/.config/yazi/plugins/funscript-prev.yazi/main.lua`)
4. Add this to your `yazi.toml`
```toml
[plugin]
prepend_previewers = [
  { name = "*.funscript", run = "funscript-prev" },
]

prepend_preloaders = [
  { name = "*.funscript", run = "funscript-prev" },
]
```

### Reference
- [audio-previewer.yazi](https://github.com/gesellkammer/audio-preview.yazi) - How the file is structured.
- [funscript-io-2](https://github.com/defucilis/funscript-io-2) - How the heatmap is visualized and colored.
