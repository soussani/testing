APARTMENT 46 — MANUAL HOSTING

This is a static, self-contained browser application. There is no ChatGPT dependency, API key, account system, database, or build step. The 3D libraries are included in index.html.

OPTION 1: RUN ON YOUR MAC
1. Extract apartment-46-manual-hosting.zip.
2. Open Terminal and type cd followed by a space.
3. Drag the extracted apartment-46-planner folder into Terminal and press Return.
4. Run:
   python3 -m http.server 8080 --bind 127.0.0.1
5. Open http://localhost:8080 in Chrome, Edge, or Safari.
6. Keep Terminal open while using it. Press Control+C to stop.
If Python is unavailable, you can try opening index.html directly in your browser. Local-file storage/download behavior varies by browser; the localhost method is preferable.

OPTION 2: PUBLISH ON YOUR OWN STATIC WEB HOST
1. Upload index.html to the site's web root, or set apartment-46-planner as the publish directory.
2. No build command is required. No environment variables are required.
3. Serve it over HTTPS using your host's normal domain setup.
4. If your host requires a strict Content Security Policy, note that this self-contained version uses inline JavaScript and CSS. Configure script/style hashes for the file or split assets before applying that policy.
5. The planner has no built-in sign-in. Use the host's private access controls if you want to restrict who can see the apartment layout.

USING THE PLANNER
- 3D orbit: drag to rotate, scroll to zoom, right-drag to pan.
- Top view: pick an object, click the floor to place it, then drag it to move.
- Select an object to edit dimensions, rotation, elevation, color and notes.
- Walk inside: drag to look; W/A/S/D or arrows to move. The room map jumps between rooms.
- Export for AI downloads a ZIP with apartment-plan.json, an interior design brief, two PNG views and a labeled SVG plan.
- Extract the ZIP, then use Import plan to load apartment-plan.json back into the planner.

SAVING AND MOVING BETWEEN DEVICES
Edits auto-save only in the current browser for the current website address. They are not synced to the host, to ChatGPT, or to another device. Changing the hostname, protocol or port creates a different browser storage area. Export before changing addresses, clearing browser data, or moving to another device. Import the JSON at the new address.

MODEL LIMITS
Main dimensions follow the supplied plan. Ceiling and opening heights, railing, beams and some wall offsets are approximate. This is a furniture-planning reference, not a surveyed construction model.
