# Arabic NLP API - Powered by ArPHP and Al-Mosahih ASC

[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)]()

A comprehensive Docker container providing REST API endpoints for Arabic language processing powered by the ArPHP library.
This repo is for techincal support purposes. You can download the image from this link: https://hub.docker.com/r/asc7team/arphpapi

## Quick Start

```bash
# Pull the image
docker pull asc7team/arphpapi:latest

# Run the container
docker run -d -p 8080:80 --name arphp asc7team/arphpapi:latest

# Test the API
curl -X POST http://localhost:8080/spell-check \
  -H "Content-Type: application/json" \
  -d '{"text":"مرحبا بكم"}'
```

## What's Inside

This container provides **15+ Arabic NLP endpoints** for:

- ✅ **Spell checking** with intelligent suggestions (powered by Al-Mosahih ASC Open Source)
- 📊 **Sentiment analysis** for Arabic content
- 🗣️ **Dialect identification** (MSA, Egyptian, Gulf, etc.)
- 🔄 **Arabic-English transliteration** (bidirectional)
- 🔢 **Number to Arabic words** with proper grammar
- ⌨️ **Keyboard layout correction** (AR/EN)
- 📅 **Hijri calendar** conversion and formatting
- 🕌 **Prayer times** calculator with Qibla direction
- 📝 **Text summarization** with keyword extraction
- 👤 **Gender detection** from Arabic names
- 🔍 **Arabic-friendly SQL** query generation
- 📊 **Text similarity** comparison
- 🎵 **Arabic Soundex** for phonetic matching

## API Examples

### Spell Check
```bash
POST /spell-check
{"text": "كتاب"}
```

### Transliterate
```bash
POST /transliterate
{"text": "marhaba", "direction": "en2ar"}
```

### Prayer Times
```bash
POST /prayer-times
{
  "latitude": 21.4225,
  "longitude": 39.8262,
  "timezone": 3,
  "elevation": 277
}
```

### Number to Arabic
```bash
POST /spell-number
{"number": 1234, "format": "money"}
```


## Use Cases

- 🛒 E-commerce platforms (Arabic product search, price formatting)
- 📱 Mobile apps (prayer times, Islamic calendars)
- 💬 Chat applications (sentiment analysis, dialect detection)
- 📰 Content management (spell checking, summarization)
- 🔎 Search engines (phonetic matching, query enhancement)
- 📊 Analytics platforms (Arabic text processing)

## Architecture

- **Base:** PHP 8.x with Apache
- **Library:** ArPHP - PHP Arabic library version 7.0

## Documentation

Full API documentation available at: `http://localhost:8080/` (when container is running)

## Tags

- `latest` - Latest stable release
- `1.0.0` - Specific version


## Support

- 📖 [ArPHP](https://github.com/khaled-alshamaa/ar-php)
- 📖 [Al-Mosahih ASC](https://arabicspellchecker.com/)


## License

GNU Lesser General Public License

---

**Made for developers building Arabic-first applications** 🚀
