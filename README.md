# Canopy structure influences vertical microclimate of old-growth and second-growth trees in a temperate montane forest

This repository contains the analysis code accompanying the manuscript above. It includes R code for processing, modeling, and visualizing vertical microclimate patterns from understory to canopy across old-growth and second-growth Douglas fir trees at the H.J. Andrews Experimental Forest.

**This repository contains code only — no data files are included.** See [Data Availability](#data-availability) below for download links.

---

## Citation

If you use this code, please cite the associated manuscript:

> Ferrari, N.C., Fleishman, E., Schulze, M., Bell, D.M., & Betts, M.G. [Year]. Canopy structure influences vertical microclimate of old-growth and second-growth trees in a temperate montane forest. *[Journal]*. [DOI]

<!-- TODO: fill in year, journal, and DOI once available -->

---

## Authors & Contact

| Role | Name | Affiliation |
|---|---|---|
| Corresponding author | Nina C. Ferrari | Oregon State University |
| Co-author | Erica Fleishman | Oregon State University |
| Co-author | Mark Schulze | Oregon State University |
| Co-author | David M. Bell | USDA Forest Service Pacific Northwest Research Station |
| Co-author | Matthew G. Betts | Oregon State University |

**Contact:** nina.ferrari@oregonstate.edu
**ORCID:** [https://orcid.org/0000-0003-4205-9708](https://orcid.org/0000-0003-4205-9708)


---

## Data Availability

Data are **not included in this repository** and must be downloaded separately from the sources below before running the code.

### Vertical microclimate & LiDAR data (EDI / H.J. Andrews Data Portal)

| File | Description | DOI |
|---|---|---|
| `mv010_1.csv` | Vertical microclimate data | [DOI LINK] |
| `mv010_2.csv` | LiDAR data | [DOI LINK] |

Both packages are archived at the [H.J. Andrews / EDI Data Portal](https://portal.edirepository.org/). License: **[CC0 / CC-BY 4.0 — confirm on package page]**.

<!-- TODO: confirm and fill in license + DOI for each package -->

### Meteorological station data (H.J. Andrews Data Portal)

**CENMET** (central reference station — represents ambient conditions):
https://andrewsforest.oregonstate.edu/sites/default/files/lter/data/weather/portal/CENMET/data/index.html
- `cenmet_234_a_5min_2022.csv`
- `cenmet_234_a_5min_2023.csv`
- `cenmet_234_a_5min_2024.csv`

**VANMET** (secondary reference station — used for QA/QC of CENMET data):
https://andrewsforest.oregonstate.edu/sites/default/files/lter/data/weather/portal/VANMET/data/index.html
- `vanmet_231_a_5min_2022.csv`
- `vanmet_241_a_5min_2023.csv`
- `vanmet_241_a_5min_2024.csv`

---

## Repository Structure

```
├── README.md
├── LICENSE
└── microclimate_analysis.R
```

---

## Requirements

- **R version used:** R version 4.5.1 (2025-06-13 ucrt)
- **Required packages:**

```r
install.packages(c(
  "broom.mixed", "cowplot", "dplyr", "hms", "emmeans", "ggcorrplot",
  "ggplot2", "gt", "lubridate", "lme4", "nlme", "patchwork", "purrr",
  "readr", "scales", "suncalc", "tidyverse", "zoo", "rlang"
))
```

---

## Usage

1. **Set up your project folder.** All data files must be placed in the same folder as the script (no subfolders) — paths in the script are relative (e.g. `"./mv010_1.csv"`).

2. **Download the data files** listed above in [Data Availability](#data-availability) and save them into that folder.

3. **Set your working directory** to that folder, e.g.:
   ```r
   setwd("C:/Users/yourname/Documents/microclimate_analysis")
   ```

4. **Run the script sections in order.** See section headers in the script for structure:
   `Packages → Data Import → Data Prep → Models → Figures → Tables`

---

## License

- **Code** in this repository is licensed under the [MIT License](LICENSE).
- **Data** referenced above are licensed separately by their respective sources (see [Data Availability](#data-availability)) — the code license does *not* apply to the data.

---

## Acknowledgments

The authors acknowledge funding from the National Science Foundation Long Term Ecological Research (LTER) program, administered cooperatively by Oregon State University, the US Department of Agriculture Forest Service Pacific Northwest Research Station, and the Willamette National Forest. This material is based on work supported by the National Science Foundation under the grant LTER8 DEB2025755.

This research was conducted at the H.J. Andrews Experimental Forest, part of the Long-Term Ecological Research (LTER) Network.
