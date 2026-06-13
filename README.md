# “I Will Not Let Colonisers Erase One Half of Me”: Queer Palestinian Muslim Visibility on *Queering the Map*

<p align="center">
  <img src="https://asapjournal.com/wp-content/uploads/2021/06/Cover-Image_screenshot.jpg" alt="Queering the Map" width="700"/>
</p>

<p align="center">
  <em>Code and data repository accompanying the research paper.</em>
</p>

---

## Authors

1. **Aisha Nazim** — University College Dublin  
2. **Dr. Elizabeth Farries** — University College Dublin  
3. **Dr. Paraic Kerrigan** — University College Dublin  
4. **Zaur Gouliev** — University College Dublin  

---

## Overview

This repository contains the code, data, and supporting materials used in the study:

> *“I Will Not Let Colonisers Erase One Half of Me”: Queer Palestinian Muslim Visibility on Queering the Map*

The project examines how queer Palestinians use the Queering the Map (QtM) platform to negotiate visibility, identity, memory, and resistance within the context of occupation, displacement, and digital self-expression.

Using a custom Python workflow, the project retrieves publicly available QtM posts from a geographically bounded region, extracts associated narratives, and prepares them for qualitative thematic analysis.

---

## Repository Contents

```text
.
├── QtM_Scraper.ipynb          # Data collection notebook
├── qtm_OPT_posts.csv          # Occupied Palestinian Territories dataset
├── qtm_palestine_posts.csv    # Palestine dataset
└── README.md
```

---

## How It Works

The scraper follows five steps:

1. Accesses the public Queering the Map GeoJSON index.
2. Filters map points using user-defined geographic coordinates.
3. Collects unique post identifiers.
4. Retrieves the corresponding narrative text for each post.
5. Exports structured datasets for qualitative analysis.

Researchers can define any region of interest through a custom bounding box.

### Example Coordinates Used in This Study

```python
# West Bank, including East Jerusalem
WB = (34.10, 31.00, 35.80, 32.85)

# Gaza Strip
GZ = (34.15, 31.18, 34.64, 31.63)
```

Each bounding box follows this format:

```python
REGION = (
    longitude_min,
    latitude_min,
    longitude_max,
    latitude_max
)
```

---

## Running the Notebook

Open the notebook locally:

```bash
jupyter notebook QtM_Scraper.ipynb
```

or:

```bash
jupyter lab
```

Then run the notebook cells sequentially.

---

## Output

The scraper exports posts in structured CSV format with the following fields:

```text
short_id
longitude
latitude
description
```

Example output:

```csv
short_id,longitude,latitude,description
138607,34.781,32.085,"Example narrative text from Queering the Map."
```

---

## Reproducibility

The code is provided to support transparent and reproducible research. The workflow can be adapted to examine other countries, cities, or regions represented on Queering the Map.

---

## Citation

If using this repository, please cite:

```text
Nazim, A., Farries, E., Kerrigan, P., & Gouliev, Z. (2026).

“I Will Not Let Colonisers Erase One Half of Me”:
Queer Palestinian Muslim Visibility on Queering the Map.
```

---

## Disclaimer

This repository is an independent academic research project and is not affiliated with, endorsed by, sponsored by, or associated with Queering the Map, its creators, contributors, or administrators.

All data accessed through this project were obtained from publicly available resources for research and educational purposes. The views, analyses, findings, and interpretations presented in this repository are solely those of the authors and do not represent the views of Queering the Map.

Users are responsible for ensuring that any use of this code or data complies with applicable laws, ethical research guidelines, institutional review requirements, and the Queering the Map Terms of Service.
