# DBI Translations and Patches
This repository contains the latest community-driven translations and patched binaries for DBI.

## 📂 Repository Structure
- `translations.csv`: The master dictionary containing all supported languages.
- **Releases**: Check the [Releases](https://github.com/rashevskyv/DBIPatcher/releases) section for the latest translated XLSX and DBI binaries.

## ✍️ How to Contribute Translations
To add or update translations, you can modify the `translations.csv` file:

1. **Locate the String**: Find the row by its Russian text in the `ru` column.
2. **Add Translation**: Update the column for your language (e.g., `uk`, `de`, `fr`).
3. **Save & Submit**: Save the file in CSV format and create a Pull Request.

### 📏 Technical Constraints
- Each string has a `max_size` (byte limit) defined in the DBI source.
- Our automation script automatically maps certain Cyrillic characters to visually identical ASCII characters (e.g., Cyrillic 'А' -> Latin 'A') to save space.
- Keep translations concise to avoid truncation.

---
*Maintained by the DBI Translation Pipeline.*
