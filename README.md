# DBI Translations Repository

This repository contains community-driven translations and patched DBI binaries.

[![GitHub release](https://img.shields.io/github/v/release/rashevskyv/DBIPatcher)](https://github.com/rashevskyv/DBIPatcher/releases/latest)

## 📦 Downloads

Pre-patched DBI binaries for each language are available in the [**Releases**](https://github.com/rashevskyv/DBIPatcher/releases) section.

---

## 📂 Repository Structure

Each language has its own CSV file containing the full translation for that language:

| File | Language |
|------|----------|
| `en.csv` | English (US) |
| `engb.csv` | English (UK) |
| `ua.csv` | Ukrainian |
| `be.csv` | Belarusian |
| `de.csv` | German |
| `fr.csv` | French |
| `frca.csv` | French (Canada) |
| `es.csv` | Spanish |
| `es419.csv` | Spanish (Latin America) |
| `it.csv` | Italian |
| `pt.csv` | Portuguese |
| `ptbr.csv` | Portuguese (Brazil) |
| `nl.csv` | Dutch |
| `pl.csv` | Polish |
| `tr.csv` | Turkish |
| `et.csv` | Estonian |
| `lt.csv` | Lithuanian |
| `lv.csv` | Latvian |
| `kk.csv` | Kazakh |
| `jp.csv` | Japanese |
| `kr.csv` | Korean |
| `zhcn.csv` | Chinese (Simplified) |
| `zhtw.csv` | Chinese (Traditional) |

Each CSV file has two columns:
- `original` — the original Russian text from DBI
- `translation` — the translated text for that language

---

## ✍️ How to Contribute

You can improve or add translations by editing the CSV file for your language directly on GitHub.

### Step-by-step guide

1. **Open the CSV file** for your language (e.g., `de.csv` for German).
2. **Find the string** you want to fix — search by the Russian text in the `original` column.
3. **Edit the `translation` column** for that row.
4. **Submit a Pull Request** with your changes.

Our automation pipeline pulls your changes automatically and includes them in the next DBI release.

### ⚠️ Technical Constraints

- **Keep it short.** Each string has a strict byte limit defined by the DBI binary. The pipeline rejects translations that are too long.
- **No line breaks** unless the original string has one. Use `\n` only where the Russian original does.
- **Placeholders like `%s`, `%d`, `{}`, `{0}`** — keep them as-is. They are replaced at runtime by actual values.
- **Special characters** — the build system automatically maps certain Cyrillic characters to visually identical ASCII equivalents (e.g., Cyrillic `А` → Latin `A`) to save space. This is done automatically; you don't need to do it manually.

### Adding a New Language

If your language is not yet listed:
1. Create a new file named `<code>.csv` (e.g., `fi.csv` for Finnish).
2. Add the two columns: `original` and `translation`.
3. Fill in as many rows as you can.
4. Open a Pull Request — we'll take care of the rest.

---

*Maintained by the [DBI Translation Pipeline](https://github.com/rashevskyv/DBIPatcher).*
