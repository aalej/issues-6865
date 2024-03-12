# Repro for issue 6865

# Versions

firebase-tools: v13.4.1<br>
node: v20.10.0<br>
platform: macOS Sonoma 14.3.1

## Steps to reproduce

1. Run the emulators
   - `firebase emulators:start --project demo-project`
2. Open "http://127.0.0.1:5000/" on a browser
3. Click the "Choose Files" btn
4. Select `img-0-1mb.png`,`img-1-1mb.png`,`img-2-1.3mb.png`,`img-3-1.2mb.png`,
5. Click "Upload" buttonn
   - Console logs show:

```
Upload files
Upload promises complete
```

6. Files should be uploaded to the Storage emulator

- "http://localhost:4000/storage/demo-project.appspot.com/temp"
