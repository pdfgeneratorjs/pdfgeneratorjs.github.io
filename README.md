# 📄 PDF Generator

A beautiful, fully client-side PDF generator that converts images into a single PDF document with smart compression capabilities. Built with vanilla HTML, CSS, and JavaScript — no backend required.

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)

## ✨ Features

- 🖼️ **Image to PDF Conversion** — Combine multiple images (JPG, PNG, WebP) into a single PDF
- 🗜️ **Smart Compression** — Reduce image file sizes to a custom target (10 KB – 10 MB) using an iterative quality + scale algorithm
- 🔄 **Re-compression Support** — Change the target size anytime; original images are preserved and re-compressed on each generation
- 📐 **Orientation Support** — Choose between Portrait and Landscape page layouts
- 📏 **Multiple Page Sizes** — A3, A4, A5, Letter, Legal
- 🌍 **Multilingual** — Ukrainian (default) and English UI
- 🎨 **Beautiful Modern UI** — Gradient design with smooth animations
- 🖱️ **Drag & Drop** — Upload files by dragging them into the upload area
- ↕️ **Reorder Images** — Drag-and-drop image cards to change PDF page order
- 💾 **Persistent State** — All settings, images, and language preferences are saved to LocalStorage and restored on reload
- 📊 **Progress Indicator** — Real-time progress bar during compression and PDF generation
- 🔔 **Toast Notifications** — Instant feedback for user actions
- 📱 **Responsive Design** — Works on desktop, tablet, and mobile devices
- 🔒 **100% Client-Side** — No data leaves your browser; all processing happens locally

## 🚀 Getting Started

### Live Demo

Try it now: **[pdfgeneratorjs.github.io](https://pdfgeneratorjs.github.io)**

### Installation

No installation required. Simply download the HTML file and open it in any modern web browser.

```bash
git clone https://github.com/pdfgeneratorjs/pdfgeneratorjs.github.io.git
cd pdfgeneratorjs.github.io
```

Then open `index.html` in your browser.

### Usage

1. **Upload Images** — Click the upload area or drag and drop image files
2. **Configure Settings**:
   - Select page **orientation** (Portrait / Landscape)
   - Choose **page size** (A3, A4, A5, Letter, Legal)
   - Enable **compression** and set a target file size in KB
3. **Reorder** — Drag images to arrange the page order
4. **Generate PDF** — Click "Create PDF" and the file will be downloaded automatically

## 🌐 Language Support

The interface is available in:

- 🇺🇦 **Ukrainian** (default)
- 🇬🇧 **English**

Switch languages using the toggle in the top-right corner. Your preference is saved automatically.

## 🛠️ Technologies Used

- **HTML5** — Semantic markup
- **CSS3** — Modern styling with gradients, flexbox, and grid
- **Vanilla JavaScript** — No frameworks or build tools
- **[jsPDF](https://github.com/parallax/jsPDF)** — PDF generation library
- **Canvas API** — Image compression and resizing
- **LocalStorage API** — State persistence

## 📂 Project Structure

```
pdfgeneratorjs.github.io/
├── index.html      # Single-file application (HTML + CSS + JS)
└── README.md       # Documentation
```

## ⚙️ How Compression Works

The compression algorithm iteratively reduces image quality and dimensions until the target file size is reached:

1. Start with original quality (92%) and full dimensions
2. If the result exceeds the target size:
   - Reduce JPEG quality in steps of 8%
   - Once quality reaches 30%, scale dimensions by 90% and reset quality to 70%
3. Repeat up to 20 iterations or until the target is met

The original image is always preserved, so changing the target size and regenerating produces fresh results from the source.

## 💾 Data Privacy

All processing happens locally in your browser. **No images or data are uploaded to any server.** Your files remain on your device at all times.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/pdfgeneratorjs/pdfgeneratorjs.github.io/issues).

## 📜 License

MIT
