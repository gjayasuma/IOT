# Internet of Things – Course Website

Static course page for **Internet of Things**, Dept. of Information Technology, JNTUGV-CEV.
Instructor: Prof. G. JayaSuma. It is a single `index.html` plus a `pdfs/` folder of course materials. No build step is needed.

Live site: https://mkk379.github.io/iot/

## What the page contains

- Header with the college logo and course title
- Instructor and course staff (photo + link)
- Course description and prerequisites
- Quick Links: syllabus, question bank, lecture outline, study notes, slides, worksheets and comics for Units 1 to 5
- Contact details (WhatsApp and email)
- Google Analytics 4 tracking (Measurement ID `G-XTJYVWXYPV`)

Built with Bootstrap 4 (loaded from a CDN), so the page needs an internet connection to look right.

## Folder structure

`index.html` and `pdfs/` must sit side by side at the top level of the repository (or the published folder).

```
index.html
pdfs/
├── Syllabus.pdf
├── IoT_Question_Bank.pdf
├── IoT_with_Applications_Lecture_Outline.pdf
├── IoT_with_Applications_Lecture_Outline.docx
├── Study-Notes-Units/       Study-Notes-Unit-1.pdf … Study-Notes-Unit-5.pdf
├── Slides-PDF/              Slides-Unit-1.pdf … Slides-Unit-5.pdf        (opens in browser)
├── Slides-Units/            Slides-Unit-1.pptx … Slides-Unit-5.pptx      (download)
├── Worksheets/              Worksheet-Unit-1.pdf … Worksheet-Unit-5.pdf  (opens in browser)
├── Worksheets-DOCX/         Worksheet-Unit-1.docx … Worksheet-Unit-5.docx (download)
├── Comic-Images/            Comics-Unit-1.pdf … Comics-Unit-5.pdf        (opens in browser)
└── Comic-Images-DOCX/       Comics-Unit-1.docx … Comics-Unit-5.docx      (download)
```

**Why both PDF and Office versions?** Browsers cannot display `.pptx` or `.docx` files; clicking such a link only downloads it. So each slide deck, worksheet and comic has a **View (PDF)** link that opens in the browser and a **Download** link for the editable original.

## Editing the page

Open `index.html` in any text editor. Sections are marked with `EDIT HERE` comments.

| What to change | Where |
|---|---|
| College, department, term | `EDIT HERE (1)`, the `<h2>` under the title |
| Instructors | `EDIT HERE (2)`; copy a whole `<td>…</td>` block to add a person |
| Course staff | `EDIT HERE (3)`; same pattern |
| Quick Links | `EDIT HERE (5)`; copy a `<li>` line to add a link |
| Contact details | `EDIT HERE (6)` |
| Analytics ID | the two lines containing `G-XTJYVWXYPV` in `<head>` |

### Adding or replacing a file

1. Put the file in the matching `pdfs/` subfolder.
2. Make sure the link in `index.html` uses the **exact same name**, including capital letters. GitHub Pages is case-sensitive, so `Slides-Unit-1.pdf` and `slides-unit-1.pdf` are different files.
3. Avoid spaces and brackets in file names. Use `-` or `_`.

To offer a file as a download rather than opening it, add the `download` attribute to the link, as the `.pptx` and `.docx` links do.

## Publishing on GitHub Pages

1. Create a **public** repository.
2. Upload `index.html` and the `pdfs` folder to the **top level**. Do not upload the outer folder, because Pages cannot find `index.html` inside a subfolder.
3. Go to **Settings → Pages** and set Source to **Deploy from a branch**, Branch to `main`, and folder to `/ (root)`. Click **Save**.
4. After 1 to 3 minutes the site is live at `https://USERNAME.github.io/REPOSITORY/`.

Each file must stay under 25 MB for browser upload. After a change, wait a couple of minutes and hard refresh (Ctrl+Shift+R).

## Analytics

Google Analytics 4 is installed in `<head>` with Measurement ID `G-XTJYVWXYPV`.

- Check it in **Reports → Realtime** while you have the live site open. The Home page banner "No data received" can take 24 to 48 hours to clear.
- Ad blockers and privacy browsers block Analytics, so test with extensions off.
- In **Admin → Data streams**, the stream URL should match the live address.
- Visits from `file://` or a local copy are not recorded reliably. Test on the live site.

## Troubleshooting

| Problem | Likely cause and fix |
|---|---|
| **404 "File not found"** on the site address | `index.html` is not at the top level of the repository, or is not named exactly `index.html`. Move it up, or re-upload. |
| A link gives 404 | The file is missing, or the name or capitalisation differs from the link. Compare the link with the file list on GitHub. |
| `.pptx` or `.docx` does not open | Expected: browsers download these. Use the **View (PDF)** link. |
| Page looks unstyled | The Bootstrap CDN could not load. Check your internet connection. |
| Analytics shows no data | See the Analytics section above. |

## Credits

Course materials: Prof. G. JayaSuma and course staff, Dept. of Information Technology, JNTUGV-CEV.
