# Information Extraction with NLP techniques at the Second Astro-COLIBRI Workshop
Data for the 2nd Astro-COLIBRI Workshop.


### How to Load Data?

After unzipping the file, you can load it as a list of dictionaries in Python:

```
import json
with open("path/to/atels/archive/atels_archive.jsonlines", 'r') as f:
    atels_json = [json.loads(l) for l in list(f)]
```

Each entry consists of a dictionary with the following keys:

- "**report_type**": A String, indicating the type of the report (ATels, GCN Circulars etc.);
- "**report_id**": An Integer, corresponding to the unique identifier of the report;
- "**title**": A String, corresponding to the title of the published report;
- "**authors**": A string, corresponding to the list of the authors;
- "**publication_date**": A Timestamp (float), corresponding to the publication time;
- "**subjects**": A List of Strings, corresponding to the type/nature of the celestial objects in the text (e.g., Supernova, Blazar etc.); 
- "**fulltext**": A String, corresponding to the report;
- "**related_references**": A List of related links (to other observation reports). Not necessary for the Workshop; 
- "**fulltext_hyperlinked_references**": A List of links (to other observation reports cited in the body of the text). Not necessary for the Workshop;

Example of an entry:

```

{'report_type': 'atel',
 'report_id': 161,
 'title': '4U 1630-47 Enters a Bright X-Ray Flaring State',
 'authors': 'John A. Tomsick (UC San Diego)',
 'publication_date': 1054047540.0,
 'subjects': ['X-ray', ' Black Hole', ' Transient'],
 'fulltext': 'The black hole candidate X-ray transient 4U 1630-47 is currently undergoing an extended outburst that began in 2002 September (see ATELs #106, #108, and #109) and has now persisted for nearly 260 days. Over the past 10 days (MJD 52,776-52,786), the source brightened from 20 c/s to over 40 c/s in the Rossi X-ray Timing Explorer ASM, and the 1.5-12 keV flux is currently near 2E-8 erg cm^-2 s^-1. As the flux increased, our RXTE/PCA observations indicate that the X-ray (3-60 keV) variability on ~10-100 second time scales increased significantly. On 2003 May 18 and May 21, the source exhibited multiple 50-100 second X-ray flares, during which the flux increased by a factor of 1.5-2.0. These flares appear to be similar to the flares seen near the start of the outburst (see ATEL #109 by Homan & Wijnands). A detailed analysis of the May 21 (MJD 52,780.7) PCA observation indicates that the other X-ray spectral and timing properties are similar to the properties at the start of the outburst. The energy spectrum is well-described by a disk-blackbody with a inner disk temperature of 1.6 keV plus a power-law with a photon index of 2.4. The power spectrum has a power-law shape with a fractional rms of 12% (0.01-100 Hz), and no QPOs are present.',
 'related_references': ['https://www.astronomerstelegram.org/?read=161',
  'https://www.astronomerstelegram.org/?read=109',
  'https://www.astronomerstelegram.org/?read=108',
  'https://www.astronomerstelegram.org/?read=106'],
 'fulltext_hyperlinked_references': []
}

```
