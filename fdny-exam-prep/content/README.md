# Content folder — add your publications here

The app ships with **sample study content only**. This folder is where you plug in your
own material. When the site is hosted (see the main README), the app fetches
`content/manifest.json` at runtime and merges your entries into the **Reference Library**
and **Diagrams & Video** views.

> ⚠️ **Copyright / distribution.** FDNY operational manuals (Communications, Probationary
> Firefighter, Regulations, HAZMAT, CFR-D, Ladder/Engine Operations, All Units Circulars)
> are distributed on the FDNY intranet and are not public. Only add copies you are
> authorized to use, and **do not commit them to a public repository**. Keep a private
> repo, or list links to an access-controlled location instead of committing the PDFs.

## How to add a publication

1. Put the PDF in this folder, e.g. `content/communications-manual.pdf`
   *(or host it somewhere you control and use a full URL instead of a local path).*
2. Add an entry to `manifest.json` under `references`:

```json
{
  "references": [
    {
      "title": "Communications Manual (2024 ed.)",
      "topic": "comms",
      "file": "content/communications-manual.pdf",
      "note": "Chapters 1–9"
    }
  ],
  "videos": []
}
```

- `topic` must match one of the built-in topic ids:
  `firecode, comms, proby, regs, hazmat, cfrd, ladder, engine, circulars, command, construction`
- Use `file` for a local PDF in this folder, or `url` for an externally hosted document.
- Entries appear in the Reference Library with a **Loaded** badge and an **Open ↗** button.

## How to add a short video

```json
{
  "references": [],
  "videos": [
    {
      "title": "Ventilation coordination",
      "topic": "ladder",
      "embed": "https://www.youtube.com/embed/VIDEO_ID"
    }
  ]
}
```

Videos render as embeds in **Diagrams & Video**. Use an `embed` URL (the player/iframe URL),
or a `url` to a file you host.

## Deepening the built-in study banks

The sample questions, flashcards, scenarios, acronyms, and podcast talking points live in
arrays near the top of `index.html` (`QUESTIONS`, `FLASHCARDS`, `SCENARIOS`, `ACRONYMS`,
`TOPIC_NOTES`). Once you have your publications, replace/extend those arrays with items
written from your material. Keep each item concise and accurate to the source.
