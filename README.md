# 🎧 Audiobook Library Player

A clean, modern, and lightweight web-based audiobook player designed for personal use. This repository serves as a **Central Hub** for your audiobook collection, allowing you to stream audiobooks hosted across multiple GitHub repositories or different servers.

## 🚀 Features

- **Centralized Library**: Manage all your audiobooks in one place via a simple `catalog.json` file.
- **Cross-Repository Support**: Stream audio files from other GitHub repositories or external URLs to bypass GitHub's storage limits.
- **Modern UI**: Dark-themed, mobile-responsive interface.
- **Smart Playback**:
  - Auto-advance to the next chapter.
  - Remembers volume settings.
  - Keyboard shortcuts (Space to play/pause, Arrows to skip 10s).
- **Format Support**: Plays both `.mp3` and `.wav` formats.

## 📂 Project Structure

```text
.
├── index.html          # Library interface (Catalog)
├── player.html         # Universal audio player
├── catalog.json        # Central database for all books
├── audio/              # Local book folder (optional)
│   ├── config.json     # Metadata/Chapters for this specific book
│   └── Chuong-1.mp3    # Audio files
└── .nojekyll           # Ensures GitHub Pages loads data folders correctly
```

## 🛠 How to Add More Books

You can add books in two ways:

### Method A: Local Folder (Same Repository)
1. Create a new folder (e.g., `books/my-new-book/`).
2. Add your audio files and a `config.json` inside it.
3. Update `catalog.json` at the root:
   ```json
   {
     "id": "my-book",
     "title": "Book Title",
     "author": "Author Name",
     "folder": "books/my-new-book",
     "cover": "books/my-new-book/cover.jpg"
   }
   ```

### Method B: Remote Repository (Bypass 1GB Limit)
1. Create a **separate GitHub repository** for the new book.
2. Upload audio files and `config.json`.
3. Enable **GitHub Pages** for that repo.
4. Add the URL to your `catalog.json` in this repo:
   ```json
   {
     "id": "remote-book",
     "title": "Remote Audiobook",
     "author": "Author Name",
     "folder": "https://username.github.io/remote-repo-name",
     "cover": "https://username.github.io/remote-repo-name/cover.jpg"
   }
   ```

## ⌨️ Shortcuts
- **Space**: Play / Pause
- **Right Arrow**: Fast Forward 10s
- **Left Arrow**: Rewind 10s

## 📄 License
MIT

---
*Developed with ❤️ for audiobook enthusiasts.*
