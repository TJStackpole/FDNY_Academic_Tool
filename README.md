FDNY Promotion Exam Prep — Study Console

A single-file, zero-install study app for firefighters preparing for the DCAS FDNY promotion exams to Lieutenant, Captain, and Chief. It runs entirely in the browser, persists your progress locally, and is built to host for free on GitHub Pages.

Not affiliated with, or endorsed by, the FDNY or NYC DCAS. All study content in this build is illustrative sample material covering general fire-service knowledge, not official exam content. Replace it with your own authorized publications (see below).
Features

Dashboard (analytics command-center) — KPIs (readiness, accuracy, streak, plan adherence), a readiness-over-time trend chart, a topic-mastery heatmap (tap a topic to drill it), study-activity bars for the last 14 days, plan-adherence tracking with a day-by-day strip, an auto-surfaced focus areas list of your weakest topics, and today's plan with a complete toggle.
Learning-Style Survey — a VARK-style questionnaire that profiles you as Visual / Auditory / Reading-Writing / Kinesthetic and biases recommendations and your plan toward the modalities you learn from best.
Study Plan Builder — enter your exam date and how many minutes you can study each day; the app generates a session-by-session schedule across topics, honoring your priority topics and preferred modality.
Reference Library — links out to the public sources (NYC Fire Code, FDNY rules, DCAS exam notices) and provides "add PDF" slots for the internal manuals you'll supply.
Flashcards — flip cards by topic; mark known / review.
Practice Test — timed, scored multiple choice in the DCAS computer-based format (70% to pass), with per-question explanations.
Daily Quiz — five questions a day that build your streak.
Scenarios — situational-judgment prompts with "what graders look for" + model answers.
Podcast Studio — pick topics + rank + length; the app assembles a script and narrates it in your browser (Web Speech API) with play/pause/stop, speed, and voice selection.
Diagrams & Video — automated visual explainers (ICS span-of-control, RECEO-VS, fire growth curve) plus embeddable slots for your own short clips.
Acronyms & Mnemonics — searchable memory hooks (RECEO-VS, SLICE-RS, COAL WAS WEALTH, LCES, LUNAR, DECIDE, BE-SAHF, …).
Run it

Locally: just open index.html in any modern browser (double-click). Everything works except the manifest auto-loader, which needs to be served over http(s) — so for adding publications, host it (below) or run a local server: python3 -m http.server then visit http://localhost:8000.
GitHub Pages (recommended): push this repo, then in Settings → Pages choose Deploy from a branch → main → / (root). Your app will be live at https://<user>.github.io/<repo>/. (You can also move everything into a /docs folder and select that instead.)
Add your publications

FDNY operational manuals are intranet-only and copyrighted — this app does not include them. When you have authorized copies, drop them in content/ and register them in content/manifest.json; they appear automatically in the Reference Library. Full schema and examples are in content/README.md.

Do not commit copyrighted manuals to a public repo. Use a private repository, or link to an access-controlled location instead of committing the files.

Data & privacy

Your learning-style profile, study plan, and progress are saved with localStorage in your own browser only — nothing is sent anywhere. Clearing site data resets the app. (If storage is unavailable, the app falls back to in-memory state for the session.)

Customize the study content

The sample banks (QUESTIONS, FLASHCARDS, SCENARIOS, ACRONYMS, TOPIC_NOTES) are plain arrays near the top of the <script> in index.html. Edit them to reflect your material once you've added your publications.

Notes on accuracy

The 2022 NYC Fire Code (Local Law 47 of 2022, effective Apr 15, 2022) is the edition currently in force and is linked from the Reference Library.
DCAS promotion exams are computer-based multiple choice; a passing score is 70%, the test counts for 50% of the final score, and seniority + awards make up the other 50%. Always confirm specifics against the current Notice of Examination for your title.
The emblem in the header is a generic placeholder (the FDNY logo is a City of New York trademark). Swap in your authorized artwork by editing the inline <svg> in the top bar.
License

MIT — see LICENSE. The license covers the application code only, not any publications, artwork, or exam material you add.
