# BotHub

Project analysis for the provided UI report `Shadow_Protocol_Report_Dark_Mode.html`.

Project summary
- Purpose: a dark/cyberpunk-styled static HTML report and dashboard that visualizes costs and operational metrics for a social media management (SMM) "farm". It includes charts, a themed UI, and an embedded AI diagnostics terminal that calls an external generative model API.
- Primary file: `Shadow_Protocol_Report_Dark_Mode.html`

Key features
- Cyberpunk/dark UI using Tailwind-like utilities and custom CSS (fonts: JetBrains Mono, Orbitron).
- Charts: uses Chart.js to render OPEX/CAPEX/proxy/anty (anti-detect browser) visualizations.
- AI Terminal: an in-page form that sends a user prompt and a Gemini API key to a Google generative language endpoint and renders Markdown responses via `marked`.

Dependencies (loaded via CDN in the HTML)
- Tailwind CSS (via `https://cdn.tailwindcss.com`)
- Chart.js (via `https://cdn.jsdelivr.net/npm/chart.js`)
- Marked (Markdown parser via `https://cdn.jsdelivr.net/npm/marked/marked.min.js`)
- Google Generative Models API endpoint is used in the page's JS and requires a valid API key to function.

How to view
- Open the `Shadow_Protocol_Report_Dark_Mode.html` file directly in a modern browser, or serve it from a local static server for correct CORS behavior:

	```bash
	# from the repository root
	python3 -m http.server 8000
	# then open http://localhost:8000/Shadow_Protocol_Report_Dark_Mode.html
	```

Security & ethics (important)
- The HTML contains content and UI elements that describe/visualize operational SMM "farm" tactics and budgetary guidance. This material can be used for activities that may be unethical or illegal (evasion, anonymity for malicious operations).
- I do NOT endorse or assist with illegal or harmful activity. If this project is intended for legitimate research, red-team testing, or defensive analysis, ensure you have proper authorization and sanitize/remove any personally actionable OPSEC instructions before sharing.
- The embedded AI terminal makes external API calls and may leak user prompts and API keys to third-party services. Do NOT paste secret credentials into the UI on untrusted systems. Consider adding server-side proxying and strict request validation if you intend to enable AI features.

Notes for maintainers
- If you want to keep only the visual/dashboard parts and remove potentially sensitive operational content, remove or rewrite the AI prompt/system instruction and the in-page operational descriptions.
- To make the page fully offline-friendly, replace CDN scripts with local copies and remove external API calls.

Contact / License
- This repository currently has no explicit license file. Add a `LICENSE` to clarify reuse terms.

Generated: November 2025 — analysis added by an automated README update.