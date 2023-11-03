# pomological
Metadata for U.S. Department of Agriculture (USDA) Pomological Watercolor Collection 

# Usage example

To display some of the metadata for an image (e.g. POM00001212.jpg) you can use:

- for the plain JSON file:

```
jq '.POM00001212.display | {title: .title | join(", "), subject: .subject | join(", "), contributor: .contributor | join(", ")}' metadata.json
```

- for the zstd-compressed JSON file:

```
cat metadata.json.zst | zstd -d | jq '.POM00001212.display | {title: .title | join(", "), subject: .subject | join(", "), contributor: .contributor | join(", ")}'
```

# Sources

- The Collection https://search.nal.usda.gov/discovery/collectionDiscovery?vid=01NAL_INST:MAIN&collectionId=81279629860007426
- Torrent of the collection (57G, somehow padded to 97G) https://archive.org/download/usda-pomological-watercolor-collection/usda-pomological-watercolor-collection_archive.torrent
