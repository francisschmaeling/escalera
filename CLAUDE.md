# Escalera

Escalera is a planned adaptive English practice app for emergent bilingual students in Texas high schools. This repo is the preview: a home page and a clickable demo with sample data, hosted on GitHub Pages.

- Live site: https://francisschmaeling.github.io/escalera/
- Demo: https://francisschmaeling.github.io/escalera/app.html
- Repo: francisschmaeling/escalera, branch `main`, folder `/` (root). Every push to `main` republishes in 1 to 2 minutes.

## Files

- `index.html`: home page, one self-contained file (about 1.5 MB, images embedded as base64).
  - Hero: cobalt sky with cloud art from the owner's mockup. The sky and the clouds are separate embedded layers. The clouds drift with a CSS animation, speed up while the page scrolls (JS sets `playbackRate`), and have light parallax.
  - Sections in order: top nav, support ladder, how a session works, mastery chart, ACE response, teacher view (language gaps and skill gaps), Texas standards table, pilot form (preview only, sends nothing), footer with the Austin skyline engraving.
  - Fonts: Inter for everything, EB Garamond for the footer wordmark and footer links.
  - Links with `data-app` point to `app.html#...` on github.io.
- `app.html`: demo app, one file, sample data only.
  - Student routes: `#/s/join`, `#/s/today`, `#/s/practice`, `#/s/respond`, `#/s/results`
  - Teacher routes: `#/t/overview`, `#/t/students`, `#/t/student/<id>`, `#/t/review/<id>`, `#/t/assign`, `#/t/texts`, `#/t/reports`
  - State is saved in `localStorage` under `escalera-demo-v1`. A small floating "Demo" switch (bottom right) moves between student and teacher views.
  - Fonts: Gelasio for headings, Inter for everything else.

## Design rules

- The app follows the owner's three original screens (teacher overview, student practice, student response): white sidebar and top bar, serif headings, the same cards in the same places. Keep that structure.
- Style is Tailwind-influenced: clean borders, consistent corners and spacing, crisp buttons and inputs.
- Keep screens light. No information overload: no stat rows, extra badges, or extra labels unless asked.
- Colors:
  - Cobalt `#0447C6` is the brand (hover `#0A3AA3`, tint `#EFF4FF`).
  - Navy `#0B2A75` for app headings. Navy `#1E3A8A` marks skill gaps.
  - Coral `#F46158` marks language support only (text `#B42318`, tint `#FFF1EE`).
  - Grays follow Tailwind's gray scale.
- Student actions carry English and Spanish labels (for example, "Check answer" with "Revisar respuesta").
- Test at phone width. The owner usually reviews on a phone.

## Writing rules

- Plain, brief copy.
- No em dashes.
- No "X, not Y" contrast sentences. Write plain statements.

## Product facts (keep copy accurate)

- After a miss, the student gets a new question on the same skill with more support each time: key words explained, then Spanish, then a worked example.
- Language gap: right once the words were explained or shown in Spanish. Skill gap: needed the worked example.
- Mastery means correct with no support. Time in the app does not count.
- Every session ends with an ACE response (Answer, Cite, Explain), written or spoken, with feedback in English and Spanish that the teacher can edit.
- Standards: English I TEKS E1.4F (inference), E1.4G (key ideas), E1.5D (summary), E1.6A (theme), and the 2024 ELPS with five levels: Pre-Production, Beginning, Intermediate, High Intermediate, Advanced. Speaking and writing tasks give TELPAS practice.
- Sample data (fictional): ESOL I, 3rd block, 20 students, teacher Ms. Ortiz, student Daniela R., week of September 28, 54 sessions, 59 language gaps and 56 skill gaps, passage "The Tryout".

## Rules for this repo

- The repo is public. Sample data only. Never add real student names or records.
- Keep `index.html` under about 2 MB so it loads on phones.
- Before pushing: open both pages, check the console for errors, and check a phone-width layout.

## Possible next steps

- Keep refining the app pages in the same look.
- Real student use needs a separate host with secure logins and a district data agreement. GitHub Pages is for the preview only.
