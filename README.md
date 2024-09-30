# AI-Powered-Drug-Discovery

## Overview

<p align="justify">
This project is designed to systematically retrieve and analyze data related to approve drugs from the ChEMBL database. ChEMBL is a highly respected chemical database that provides bioactive molecule information, making it a valuable resource for drug discovery and research. The primary focus of this project is to extract key information, such as the date of drug approval and the corresponding SMILES (Simplified Molecular Input Line Entry System) notation, which serves as a textual representation of the chemical structures. This project aims to facilitate deeper insights into the drug discovery through fine tuning of LLM on retrieval data of ChEMBL.

## Key Features

- **Comprehensive Data Retrieval:** The project employs advanced data retrieval techniques to efficiently gather a wide array of data from the ChEMBL database, specifically targeting drugs that have achieved full approval status. This includes critical identifiers and chemical structure information that are foundational for research.

- **SMILES Notation Extraction:** SMILES notation is a compact and widely used chemical notation. The project extracts and stores this information for each approved drug, enabling easy analysis and integration into molecular modeling tools.

- **Approval Timeline Analysis:** By capturing the approval dates of each drug, the project allows for the creation of temporal insights, helping to understand trends and shifts in drug approvals over time.

- **Fine Tuning of LLM (ChatCohere):** The retrieval data is stored in CSV file and use to fine tune the Cohere LLM. The LLM provides the preferred name of drug, detailed information of the target drug, and the structure of the drug. 

- **Interactive Web Interface (gardio):** Provides user_friendly web interface whereuser/chemist can easily enter the ChEMBL ID and SMILES of the drug and receives drug target information along with drug structure as well as preferred name of the drug. 

## Technical Components

- **Libraries:** Datamol, Chembl_warehouse_client, Pandas, ChatCohere
- **APIs:** Cohere
- **Web Framework:** Gardio

## Workflow

- **User Input:** ChEBL ID and SMILES of a drug is provided through gardio interface.

- **Drug Target Information:** Cohere LLM is queried to provide drug target information. This information includes a detailed summary of the drug's known biological target and its mechanism of action. It also provides approaches towards the synthesis of new compounds approaching novel drugs for multi targets, give chemical and physical properties of the drug as well. Moreover, it provides target protein structures and formulas for the drug.

- **Output:** Drug target information, preferred name of the drug, and molecular structure of the drug are presented to user 
