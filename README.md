# Found on the Oval · 8th Wall field test

This version reuses the GPS navigation and both GLB models from the original project. The new camera mode runs in the phone browser using the 8th Wall distributed SLAM engine and Three.js. No cloud editor account or build step is required. Internet access is needed for the CDN dependencies.

## Test on a phone

1. Serve the contents of this directory over HTTPS. Keep `index.html`, `app.js`, `ar.js`, `ar.css`, and `models/` together.
2. For an indoor camera check, open the HTTPS page with `?preview=1` (ashtray) or `?preview=2` (laptop).
3. Tap **Open camera AR**, allow the camera and any motion permission requested by the browser, and slowly sweep the camera over a textured floor or pavement.
4. Aim the circle at the ground and move the phone slowly. Once tracking is stable, the object appears automatically. Walk around it. The ashtray plays three loops and stops. The laptop waits four seconds after placement and then loops.
5. For the Oval walkthrough, open the page without a query string, tap **Start**, allow location access and walk to either test coordinate in `app.js`. The desktop-only demo route is still available with `?fake`.

The app uses GPS to unlock each model and local SLAM to hold the automatically chosen ground placement for the current camera session. A new camera session places the object again when tracking is stable. The cigarette and ashtray are set to 40.000055, -83.010448; the laptop is set to 39.999360, -83.014299. Phone GPS may drift by several metres, so these coordinates do not guarantee centimetre-accurate placement at the exact point. The two real-world model widths are approximate and editable in `app.js`.

## References

- 8th Wall Engine overview: https://8thwall.org/docs/engine/overview
- 8th Wall Three.js World Effects example: https://github.com/8thwall/threejs-world-effects-example
- Engine license information: https://8thwall.org/docs/open-source
- Original project: https://github.com/benfitz1110-dev/myproject-oak-tree
