# Netlify EmulatorJS ROM Player

This is a static site you can deploy directly to Netlify.

## Files

- `index.html`: the ROM player UI.
- `_headers`: Netlify headers for SharedArrayBuffer / WebAssembly support.
- `roms/`: put your game ROMs here if you want hosted mode.
- `bios/`: put BIOS files here if your core/game needs them.

## Metal Slug X / Neo Geo arcade

For a typical Metal Slug X arcade dump:

```text
roms/mslugx.zip
bios/neogeo.zip
```

Then open the deployed site and press **Start hosted ROM**.

If you do not want to deploy the ROM publicly, use **Choose ROM from this computer** instead.

## Netlify deployment

Drag this whole folder into Netlify Drop, or push it to a Git repository connected to Netlify.

No build command is needed. The publish directory is the project root.

## Local test

Use a local web server. Do not open `index.html` as a `file://` URL.

For example:

```bash
python3 -m http.server 8888
```

Then open:

```text
http://localhost:8888
```

Some browser features work better over HTTPS. Netlify gives you HTTPS automatically.
