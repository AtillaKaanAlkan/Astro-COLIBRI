# Astro-COLIBRI
Data for the 2nd Astro-COLIBRI Workshop.


#### Load Data

Load data as a list of dictionaries in Python:

```
import json
with open("path/to/atels/archive/atels_archive.jsonlines", 'r') as f:
    atels_json = [json.loads(l) for l in list(f)]
```

Each entry consists of a dictionary with the following keys:

- "report_type": A String, indicating the type of the report (ATels, GCN Circulars etc.);
- "report_id": An Integer, corresponding to the unique identifier of the report;
- "title": A String, corresponding to the title of the published report;
- "authors": A string, corresponding to the list of the authors;
- "publication_date": A Timestamp (float), corresponding to the publication time;
- "subjects": A List of Strings, corresponding to the type/nature of the celestial objects in the text (e.g., Supernova, Blazar etc.); 
- "fulltext": A String, corresponding to the report;
- "related_references": A List of related links (to other observation reports). Not necessary for the Workshop; 
- "fulltext_hyperlinked_references": A List of links (to other observation reports cited in the body of the text). Not necessary for the Workshop; 
