# Metadatata replacements for flibusta archive

this data used for fb2_srv -- opds server over zips with fb2s

filename of file with replaces format -- `zipname.zip.replace`

replaces format (json):

```json
{
  "book-filename": {
    "author": {"last-name": "Author", "first-name": "Example"},
    "book-title": 
  },
    ...
}
```

For every book-filename (example: `124312.fb2` or `directory/file.fb2` if something changes) may be added fields from `FictionBook.description.title-info`.

If you have some troubles with fb2 structure or useful field names - use `xmltojson.py` on several different fb2's:

    ./xmltojson.py 1234.fb2 > 1234.json

On debian/ubuntu useful libraries will be installed by `apt update; apt install -y python3-xmltodict python3-bs4`
