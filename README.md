# HandWrite

Version: 0.1.0

HandWrite is a small PyQt5-based handwriting page generator. It renders input text as hand-like characters and exports pages as image files. This README contains only local usage and configuration notes — no external links.

## Quick summary

- GUI-based handwriting page generator
- Configuration for paper size, font, spacing and several disturbance parameters to simulate handwriting variability
- Output: image files (PNG) exported to the outputs/ folder by default

## Requirements

- Python 3.12+
- Dependencies listed in pyproject.toml (use your environment/venv to install them). Example (from project root):

```pwsh
python -m pip install -r requirements.txt
```

## Launching the application (GUI)

1. Activate your Python environment.
2. From the project root directory, run:

```pwsh
python main.py
```

3. The application window will open. Main controls are grouped as follows:
   - Paper width / height: set page size in pixels.
   - Font selection: choose a TTF file from 	tf_library/.
   - Font size: set the nominal font size (should be smaller than line spacing).
   - Line spacing / letter spacing: adjust vertical and horizontal spacing.
   - Margins: set top/ bottom / left / right margins for the page.
   - Color / background: choose text color and page background (transparent background supported).
   - Disturbance parameters: small random offsets for line spacing, font size, glyph position and rotation to mimic handwriting.
   - Export: renders the current preview to images and saves them into the outputs/ directory.

## Files and folders

- main.py — application entry point (GUI launcher).
- core.py, 	ools.py — core logic and helpers.
- 	tf_library/ — local folder for .ttf font files. Place any .ttf files you want to use here.
- outputs/ — default output directory for generated pages. Ensure this folder is writable.

## Typical workflow

1. Place desired fonts (.ttf) into 	tf_library/.
2. Start the app: python main.py.
3. Paste or type the text to render in the input area.
4. Set paper size, margins, font, font size and spacing.
5. Optionally increase disturbance parameters to make handwriting more natural.
6. Click Export. Check the outputs/ folder for generated PNG files.

## Troubleshooting

- If the app fails to start, confirm you installed dependencies and are using Python 3.12+.
- If fonts don't appear or rendering fails, ensure the font files are valid .ttf files in 	tf_library/.
- If export fails due to permissions, check that outputs/ exists and is writable.

## Notes

- This README purposely omits external links and mirrors only local usage steps.
- If you want a script to keep README.md version in sync with pyproject.toml or to generate a version badge, tell me and I can add a small helper script.
