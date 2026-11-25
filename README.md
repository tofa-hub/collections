# tofa-hub 🎬

Curated JSON collections and watch-order lists for **[tofa](https://tofa.tv)** media servers.

## 📋 Available Lists

| Collection | Type | Description | Raw URL (for tofa import) |
| :--- | :--- | :--- | :--- |
| **Disney Classics: Complete 62** | Movies | All 62 Disney Classics (1937–2024) in chronological order. | `https://raw.githubusercontent.com/tofa-hub/collections/refs/heads/main/disney-classics-62.json` |
| **The Terminal List Universe** | Shows | Jack Carr's Terminal List universe in chronological timeline order. | `https://raw.githubusercontent.com/tofa-hub/collections/refs/heads/main/the-terminal-list-universe.json` |
| **Yellowstone Universe** | Shows | Taylor Sheridan's Yellowstone & Western Universe in timeline order. | `https://raw.githubusercontent.com/tofa-hub/collections/refs/heads/main/yellowstone-universe.json` |

---

## 🚀 How to import into tofa

1. Copy the **Raw URL** of the list you want from the table above.
2. Open your **tofa** web interface.
3. Go to **Browse** → **Collections** → **Import list** (or paste the URL in the list importer).
4. tofa will automatically fetch the titles and keep the collection synced when this list is updated.

---

## 🛠️ Contributing a new list

1. Create a new `.json` file in the root of this repository (use lowercase and hyphens, e.g., `studio-ghibli.json`).
2. Follow the `tofa_list` format:

```json
{
  "tofa_list": 1,
  "name": "Collection Name",
  "description": "Short description shown under the collection's name.",
  "sort": "list",
  "items": [
    { "imdb_id": "tt0133093", "type": "movie", "order": 1 },
    { "imdb_id": "tt0903747", "type": "show", "order": 2 }
  ]
}
```

3. Commit your changes. A GitHub Action will automatically verify that the JSON syntax and required fields are valid.
