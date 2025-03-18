# Scoping petrochemicals in Southeast Asia

This repository holds data on petrochemical project and financing in Southeast Asia, from the London Stock Exchange Group (LSEG) Data & Analytics, formerly Refinitiv, as of 15 November 2024.

The data will be analyzed and used for a scoping report produced for and published by the [Center for Energy, Ecology, and Development (CEED)](https://ceedphilippines.com/). 

## Working file

Datasets downloaded from LSEG Refinitiv were *manually* sanitized and merged with previous datasets. This allows more control over the verification and deduplication of data points and line items. 

`wf_data.xlsx` is the main working file and contains the clean data. It contains the following sheets:

| Sheet name | Content |
| -------- | ------- |
| docs | information on data source, date working data was downloaded (date accessed), and list of sheets |
| pf_projects | main dataset for project finance data; does not include developer information |
| pf_developers | holds developer- and sponsor-related information |
| loans_list | main dataset for loans |
| loans_banks | holds banks-related information |
| bonds_list | main dataset for bonds |
| bonds_banks | holds banks-related information |
| eq_list | main dataset for equities |
| eq_banks | holds banks-related information |

**Important:** All amounts are in millions USD.

## Analysis

Run the `analysis-debt-financing` for analysis of bonds, equities, and loans. Run `analysis-proj-finance` for analysis of project financing. 

These notebooks will export the following datasets, which can be used for secondary and independent analysis:

| Branch | Filename | Content |
| -------- | ------- | ------- |
| bonds_data | `bonds_banks` | underwriter's parent company, country, and number of underwritings |
| bonds_data | `bonds_count` | borrower's parent company, country, number of underwritings, and total amount |
| equities_data | `equities_banks` | underwriter's parent company, country, and number of underwritings |
| equities_data | `equities_count` | borrower's parent company, country, number of underwritings, and total amount |
| loans_data | `loans_banks` | underwriter's parent company, country, and number of underwritings |
| loans_data | `loans_count` | borrower's parent company, country, number of underwritings, and total amount |
| pf_data | `pf_count` | country, number of projects financed, total cost, and average cost per project |
| pf_data | `pf_devs` | project developer's parent company, country, and number of projects |
| pf_data | `pf_false_sol_country` | country with petrochemical projects tagged as "false solutions", number of "false solutions" projects, total number of projects, and percentage of "false solutions" projects |
| pf_data | `pf_false_sol_developer` | project developer's parent company, country headquarter of project developer's parent company, project name, and country where project is located |
| pf_data | `pf_false_sol_state-owned` | state-owned project developer (parent company), country of state-owned developer, project name, and country where project is located |

Projects tagged as "false solutions" involved the following keywords: ammonia, hydrogen, and carbon capture.

## Google Colab

A Google Colab version of this repository is available [for viewing through this link](https://drive.google.com/drive/folders/10Oy2_3GAplEIis0Iq0v1YF9c3TD3Wy4r?usp=drive_link). (Only select CEED staff have editing access.)
