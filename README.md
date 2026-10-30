# 🗂 Anki Clean Edit — External WYSIWYG Editor for AnkiDroid

**Anki Clean Edit** is a fast, distraction-free, vibecoded, external WYSIWYG HTML card editor designed specifically for **AnkiDroid** on Android tablets and smartphones. 

Instead of editing raw HTML tags inside AnkiDroid's default editor, **Anki Clean Edit** automatically opens whenever you tap **Edit Note** or **＋ (Add Note)** in AnkiDroid—giving you rich formatting, a dedicated Cloze workflow, live screen capture with cropping, and 100% offline OCR.

---

## ✨ Key Features

* **⚡ Instant Auto-Open & Smart Deck Detection:**
  Automatically launches when opening the note editor in AnkiDroid (from the Deck Picker, Reviewer, or Card Browser) with your active **Note Type** and **Deck** pre-selected. Supports Split-Screen and Floating Window bounds out of the box.
* **🧩 Advanced Cloze Deletion Workflow:**
  * **`[...]+`** — Wraps selected text or a tapped image in the next cloze number (`c1` → `c2`).
  * **`[...]=`** — Wraps selection using the same cloze number as the highest existing cloze.
  * **`[...]-`** — Removes cloze brackets from selected text/image or the last cloze in the field.
  * **`[123]` (Smart Cloze Sort)** — Renumbers all clozes across your card in reading order (`c1, c2, c3...`) while preserving existing groupings (identical cloze numbers stay grouped together).
  * **Missing-Cloze Guard** — Warns you before saving a Cloze card without `{{c1::...}}` syntax.
* **🖼 Image Resizing, Cropping & Text Wrapping:**
  * Insert images from the clipboard or gallery.
  * Tap any inserted image to scale (`25%`, `50%`, `75%`, `100%`), drag the corner handle (`◢`) for smooth custom resizing, re-crop in place (`✂️ Crop`), or set **Text Wrap** (`Inline`, `Left`, `Center`, `Right`).
* **📸 Live Screen Capture & 100% Offline OCR:**
  * Capture lecture slides or PDFs directly behind the editor in Split-Screen mode.
  * Crop any region to **Copy (`📋`)**, **Insert as Image (`🖼`)**, or **Extract Text (`📝 OCR`)** offline via Google ML Kit (automatically detects larger headings and formats them in bold/title size).
* **🧹 Smart Paste & Auto-Arrows:**
  * Strips messy background colors and broken inline styles when pasting from PDFs or websites while keeping headings and bold text intact.
  * Automatically converts `->`, `<-`, `<->`, `=>`, `<=>` into `→`, `←`, `↔`, `⇒`, `⇔`.
* **👁 Interactive Single-Card Preview:**
  * Step through individual cloze numbers (`◀ Prev` / `Next ▶`) with a sticky top bar or tap **`👁 Reveal All`** to highlight all clozes in color with `c1`/`c2` badges.
* **🔒 100% Offline & Privacy-First:**
  * Hard-blocks all internet permissions (`android.permission.INTERNET` removed at manifest level). Only interacts with the `com.ichi2.anki` package.

---

## ⌨️ Hardware Keyboard Shortcuts (Tablet Book Cover / Bluetooth Keyboard)

| Shortcut | Action |
| :--- | :--- |
| **`Ctrl + Enter`** | Save Card |
| **`Ctrl + Shift + C`** | Insert Next Cloze (`[...]+`) |
| **`Ctrl + Shift + Alt + C`** | Insert Same Cloze (`[...]=`) |
| **`Ctrl + Shift + S`** | Sort Clozes Numerically (`[123]`) |
| **`Ctrl + P`** | Open Interactive Card Preview |
| **`Ctrl + Z`** / **`Ctrl + Y`** | Undo / Redo |
| **`Esc`** | Cancel / Close Editor |

---

## 🛠 Installation & Setup Guide

1. **Download & Install:**
   Download the latest **`AnkiCleanEdit.apk`** from the [**Releases**](../../releases) section and install it on your Android device.
2. **Grant AnkiDroid Database Permission:**
   Open **Anki Clean Edit** once and allow **AnkiDroid Database Read/Write** access so the app can load and save your cards.
3. **Enable Auto-Open (Accessibility Service):**
   * Tap **`❓`** inside the app → **Open Accessibility Settings** (or long-press the **`⟳ Recent`** button).
   * Go to **Installed Apps** → **Anki Clean Edit Auto-Open** and toggle it **ON**.
   * *(Tip: Exclude Anki Clean Edit from Android's "Deep Sleep" / battery optimization so Auto-Open stays responsive).*

---

## ⚠️ Known Technical Limitations

* **External AnkiWeb Images in the Editor:**
  Because the Google Play Store version of AnkiDroid stores media inside Android's protected `/Android/data/com.ichi2.anki/` sandbox, third-party apps cannot read images synced down from AnkiWeb.
  * Clean Edit displays these images as a clean blue badge (`🖼 Anki Image: ...`) inside the editor.
  * **Your images are never lost:** Their original HTML tags, filenames, and custom widths remain **100% intact** when you save and are fully visible when studying in AnkiDroid, AnkiWeb, and Anki Desktop.
  * Images you insert or screenshot directly via Clean Edit are mirrored locally (up to 300 MB) and remain fully visible and editable inside the editor.
* **Image Occlusion & Audio Recording:**
  Image Occlusion notes are automatically skipped so you can edit masks natively in AnkiDroid. To record audio on a regular card, tap **`⏸ Auto`** → **Edit THIS Card in AnkiDroid**.
