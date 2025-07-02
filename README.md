# Hiragana-to-Russian Transliteration System

This project is a **transliteration system for Japanese Hiragana**, converting it into Russian pronunciation using Unicode-based rules and context-sensitive logic.
Japanese pronunciation and transliteration are **highly context-dependent**. A rule-based transducer allows accurate modeling of the following phenomena:


## How It Works

- The input is a sentence **written in Hiragana**, read from a file (using Unicode characters).
- The sentence must consist only of **valid Hiragana characters and spaces**. Any other character is considered invalid.
- The transliteration engine uses **Unicode character IDs** to parse and transform the input.



## Key Rules Implemented

- **Sokuon (small っ)** doubles the following consonant. It cannot appear at the start or end of a word, or before a vowel.
- **N → M** before bilabials (P, F, B, M). Sokuon doubling applies *after* this change.
- **Vowel reduction**: 'I' and 'U' are reduced to 'Ь' and 'Ъ' between two voiceless consonants.
- **Terminal U-drop**: 'U' at the end of a 'су' suffix is dropped.
- **Small vowels** appear only after syllables with a "consonant + I" pattern and form a new syllable.
- **Vowel lengthening**:
  - Repeating the same vowel → long vowel  
  - E + I → long E  
  - O + U → long O  



## Try it

You can **run the transliterator and see how it works** in the notebook:  
**`transliterator.ipynb`**
