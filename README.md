# CandiData 2024: Social Media Handle Data for 2024 U.S. Federal Election Candidates

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![DOI](https://img.shields.io/badge/DOI-10.3886%2Fsqhd--kv39-blue)](https://doi.org/10.3886/sqhd-kv39)

## Overview

CandiData 2024 is a publicly available dataset of social media handles for all candidates in the 2024 U.S. federal elections, including candidates for President, U.S. Senate, and U.S. House of Representatives. The dataset covers both incumbents and non-incumbents across ten social media platforms — mainstream and alternative — and includes candidate demographic and electoral attributes to facilitate linkage with other datasets.

**This repository** contains the handles and candidate attributes dataset (CSV) and its accompanying codebook. The full social media posts dataset (~3.1 million posts) is available separately through the Social Media Archive at ICPSR (see [Accessing the Posts Data](#accessing-the-posts-data) below).

---

## Contents of This Repository

| File | Description |
|------|-------------|
| `candidata_2024_handles.csv` | Candidate attributes and social media handles for all 2024 U.S. federal candidates |
| `codebook.csv` | Variable names, descriptions, formats, and sources for all fields in the handles dataset |

---

## Dataset Description

### Platforms Covered

CandiData includes social media handles from ten platforms:

**Mainstream:** Facebook, Instagram, Threads, TikTok, Twitter/X, YouTube

**Alternative:** Gettr, Rumble, Telegram, Truth Social

For incumbents, both office accounts and campaign accounts are collected separately. For non-incumbents, only campaign accounts are included. Alternative platform handles (Truth Social, Gettr, Rumble, Telegram) were collected for Republican candidates only, as Democratic candidates are rarely present on these platforms.

### Candidate Attributes

The dataset includes the following types of variables for all candidates where available:

- **Identity & demographics:** Name, state, district, party affiliation, race, gender
- **Electoral context:** Incumbency status, office sought, district competitiveness (2024 Cook Report scores for House; 2020 presidential vote share for Senate)
- **FEC identifiers:** FEC candidate ID

For incumbents running for re-election, the dataset additionally includes:

- Birth year
- Congressional Bioguide ID
- ICPSR ID
- First-dimension DW-NOMINATE ideology score



### Posts Data Summary

In addition to handles, a companion dataset of organic social media posts from these candidates is available separately. That dataset contains approximately **3.1 million posts** collected from January 1, 2023 through December 31, 2024. Posts data was collected via [Junkipedia](https://www.junkipedia.org/), a tool built by the Algorithmic Transparency Institute for public-interest social media monitoring.

Post-level variables include post content, publish timestamp, engagement metrics (likes, views, replies, shares), and a link to full platform metadata via Junkipedia.

---

## Accessing the Data

### Handles Data (This Repository)

The candidate attributes and handles dataset is publicly available here on GitHub. Download `candidates.csv` directly or clone the repository.

### Interactive Dashboard

An interactive dashboard for exploring aggregated patterns in the data is available at [https://www.candidata24.org](https://www.candidata24.org).

### Accessing the Posts Data

The full posts dataset is hosted through the **Social Media Archive (SOMAR) at the Inter-university Consortium for Political and Social Research (ICPSR)**. To access the posts data:

1. Visit SOMAR at [https://socialmediaarchive.org](https://socialmediaarchive.org)
2. Search for "CandiData 2024" or use the DOI: [https://doi.org/10.3886/sqhd-kv39](https://doi.org/10.3886/sqhd-kv39)
3. Submit an access request through ICPSR

The data is available in CSV and JSON formats, which are compatible with standard data analysis tools in R, Python, and other languages.

---

## Data Collection and Validation

Social media handles were initially compiled from a candidate list provided by the Center for Tech and Civic Life (CTCL), which included Twitter, Facebook, YouTube, and Instagram accounts for primary candidates. Research assistants (RAs) then expanded and validated this dataset by:

- Confirming or correcting existing handles
- Identifying handles on additional platforms (TikTok, Threads, and alternative platforms)
- Using official sources (candidate campaign and office websites), platform search tools, and web search

Each handle underwent a **two-stage validation process**: a second RA independently confirmed each account by cross-referencing official websites, platform verification indicators, follower context, and news media references. Handles with uncertain validity were escalated to a project author for final determination. To be included in the final dataset, a handle must have been validated by at least two separate coders.

Candidate identifiers (Bioguide IDs, ICPSR IDs, FEC IDs, etc.) were validated by merging on state, district, last name, and first initial, with manual review of all cases that did not merge cleanly.

---

## Data Limitations

Researchers should be aware of the following limitations:

- **Platform volatility:** Social media data is subject to change. Candidates may delete posts or accounts (particularly after losing an election), meaning links to original posts may become invalid over time.
- **Engagement metrics:** Engagement figures reflect the counts at the time of collection and do not capture subsequent activity.
- **Alternative platform coverage:** Truth Social, Gettr, Rumble, and Telegram handles were collected for Republican candidates only.
- **Incomplete demographic data:** Race and gender are not available for all candidates.
- **Organic posts only:** The posts dataset excludes paid advertisements.

---

## Citation

If you use CandiData in your work, please cite:

> Brown, M. A., Lukito, J., Macdonald, M., Dowling, K., Hickey, C., & Miranda, M. (2024). *Candidata: U.S. 2024 elections candidates and social media posts* [Unpublished working paper]. https://static1.squarespace.com/static/66a13da7bfbb462aa85a0926/t/6724fa9c2484c501ce3dc62a/1730476700431/candidata2024_data_paper.pdf

---

## Partners

CandiData was assembled through a partnership between:

- [National Conference on Citizenship](https://ncoc.org)
- [Center for Tech and Civic Life](https://www.techandciviclife.org)
- [Media and Democracy Data Cooperative](https://mddatacoop.org)
- [Social Media Archive (SOMAR) at the University of Michigan](https://socialmediaarchive.org)
- Political Science Department, University of Kentucky

Handle data for Facebook, Instagram, Twitter/X, and YouTube was collected by CTCL. Additional handles for TikTok, Gettr, Rumble, Telegram, and Truth Social were collected by CandiData research assistants. Validation support was provided by partners at The Carter Center.

---

## Contact

We would love to hear how you use this data. Send questions, bug reports, and project updates to [kaitlyn@ncoc.org](mailto:kaitlyn@ncoc.org).

---

## License

This dataset is released under a [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/) license. You are free to share and adapt the data with attribution, provided that derivative works are distributed under the same license.
