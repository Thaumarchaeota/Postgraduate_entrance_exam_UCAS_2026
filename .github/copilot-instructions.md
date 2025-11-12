Repository purpose
This repository is a collection of postgraduate exam study notes (Markdown) for subjects like 101, 612, 852. Files are human-authored study content, not a software project. AI agents should treat content edits as documentation/content work (preserve intent, tone and language — Chinese).

Quick layout (what to know)
- Top-level Markdown files are the primary content (examples: `612_0-真题.md`, `852_0-真题.md`, `README.md`).
- Filenames use a numeric prefix that encodes subject and ordering: `<subject>_<index>-<brief-title>.md` (e.g. `612_1-蛋白质化学.md`). Keep that pattern when adding files so the index ordering is preserved.
- `attachments/` contains images referenced by Markdown using relative paths (e.g. `![image](attachments/aa.svg)`). Add new images into this folder and reference them relatively.
- `Ref/` contains large reference PDFs and should be treated as read-only unless explicitly asked (examples: `Ref/612_真题解析_15-24.pdf`).

Authoring / editing conventions (concrete)
- Metadata in headings: many subsections append question-year/type tags like `(16M, 21P)` or `(19P, 20X, 21P)` — preserve this format when adding or editing question/answer items. These codes are used throughout: M = 名词解释, X = 选择, T = 填空, P = 判断, J = 简答, L = 论述 (see `README.md`).
- Heading levels: content commonly uses 4-6 `#` levels (e.g. `#### 蛋白质化学`, `###### 等电点 (16M, 21P)`). Follow existing markup depth for new content.
- Citations: maintain the inline reference style used in notes (book title + page numbers, or `> quote` blocks). Do not remove or alter citation lines unless correcting factual typos.
- Images: reference images with relative paths. When adding new diagrams, put the file in `attachments/` and use `![alt](attachments/your.svg)`.
- Mathematical notation: TeX-like inline math appears in files (e.g. `$λ_{max}$` or block math). Preserve these formats.

Examples from repository (use these as templates)
- Question tag example: `###### 等电点 (16M, 21P)` — include similar parentheses for year/type when adding exam items.
- Image example: `![image](attachments/aa.svg)` (see `612_0-真题.md`).
- Reference PDF: `Ref/612_真题解析_15-24.pdf` — consult these when verifying answer keys.

> No build / test steps
- This is a content repository. There are no build scripts, test suites, or CI commands to run. Use a Markdown previewer in your editor (VS Code) to validate formatting.

Commit and PR guidance for agents
- Make focused edits with clear commit messages (one subject per PR when possible). Example commit subject: `notes(612): add 612_21-蛋白质修饰.md — 背诵题与图`.
- Avoid large sweeping rewrites of existing answers without subject-matter confirmation.

What not to change
- Do not modify files in `Ref/` (PDFs) or `612_0-大纲.pdf` unless explicitly requested.
- Preserve original Chinese wording and educational tone. Corrections for obvious typos and minor formatting fixes are acceptable, but major rephrasing should be avoided unless asked.

If you need to add new structure
- New subject files: follow `<subject>_<index>-<title>.md` and add any images to `attachments/`.
- If you add many images, create a subfolder under `attachments/` named by subject (keep relative links working).

When in doubt
- Prefer conservative edits: add new files or append clearly-labelled sections rather than rewriting. Leave a short NOTE block when you add or alter content explaining why.

Contact/verification
- For factual changes (answers or interpretations), flag the PR for human review and reference `Ref/` PDFs or the textbook citations used across files.

If you want further details
- Tell me which file(s) you plan to edit and I will extract the local conventions from those files and update these instructions.
