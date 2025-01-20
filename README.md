# Language Detection Script

This project is a simple TypeScript implementation of a language detection script using the `langdetect` library. The script identifies the language of a given text input and maps it to its full language name using a predefined dictionary.

## Prerequisites

- Google Colab account
- `langdetect` library installed within the Colab environment

## Setup in Google Colab

1. Open a new notebook in Google Colab.
2. Install the `langdetect` library by running the following cell:

   ```python
   !pip install langdetect
   ```

3. Create a cell to write and run the main script.

## Script Usage

### Main Script

Below is the Python implementation of the script:

```python
# Importing the langdetect library
from langdetect import detect

# Function to detect the language of a sentence
def detect_language(text):
    return detect(text)

# Dictionary of some famous languages and their respective codes
codes = {
    'ar': 'Arabic',
    'sq': 'Albanian',
    'bn': 'Bangla',
    'bh': 'Bhojpuri',
    'bg': 'Bulgarian',
    'cs': 'Czech',
    'da': 'Danish',
    'de': 'German',
    'en': 'English',
    'fr': 'French',
    'el': 'Greek',
    'hi': 'Hindi',
    'id': 'Indonesian',
    'it': 'Italian',
    'ja': 'Japanese',
    'kn': 'Kannada',
    'ko': 'Korean',
    'la': 'Latin',
    'mr': 'Marathi',
    'ml': 'Malayalam',
    'nl': 'Dutch',
    'te': 'Telugu',
    'ta': 'Tamil',
    'cy': 'Welsh'
}

# Example usage
text = "വനക്കമ്"  # Malayalam for "Hello"
language_code = detect_language(text)
language = codes.get(language_code, "Unknown Language")

print(f"The language of the text is: {language}")
```

### Example Output

For the input text `"സുഖമാണോ"`:

```
The language of the text is: Malayalam
```

## Notes

- The `langdetect` library may not always return accurate results for short or ambiguous text. It works better with longer sentences.
- Update the `codes` dictionary as needed to include additional languages or correct mappings.

## Contributing

Contributions are welcome! Feel free to suggest changes to improve functionality or fix bugs.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
