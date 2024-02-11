# Emoji List Repository 😀

This repository contains a JSON file with a list of emojis, their associated keywords, Unicode, categories, and text representations. It is designed to be easily used in JavaScript and Python applications.

## Source

The emoji data is sourced from the Unicode Consortium's Full Emoji List, v15.1, which can be found [here](https://unicode.org/emoji/charts/emoji-list.html).

## File Format

The data is stored in a JSON file with the following structure:

```json
[
  {
    "emoji": "😀",
    "unicode": "U+1F600",
    "text": ":grinning_face:",
    "category": "Smileys & Emotion",
    "subcategory": "face-smiling",
    "keywords": ["grinning", "face", "smile"]
  },
  // ... more emoji entries
]
```

## How to Use
### JavaScript
To use this data in your JavaScript code, you can import the JSON file and search through the emojis based on keywords, Unicode, or text representation.

```js
const emojis = require('./path-to-emoji.json');

// Example: Find an emoji by keyword
const keyword = 'smile';
const emoji = emojis.find(e => e.keywords.includes(keyword));
console.log(emoji);
```

### Python
In Python, you can load the JSON file using the json module and perform similar searches.

```python
import json

# Load the emoji data
with open('path-to-emoji.json', 'r') as file:
    emojis = json.load(file)

# Example: Find an emoji by keyword
keyword = 'smile'
emoji = next((e for e in emojis if keyword in e['keywords']), None)
print(emoji)
```
