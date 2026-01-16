# Project-16-01
This project contains every Notebook used during my research project. 
Here's a description of what they do and which csv. they're associated to :
---

### 1. Nettoyage_CAIRN2.ipynb

**Purpose**  
Cleaning of articles extracted from Cairn.

**Input**
- `fichier_res_cairn.csv`

**Output**
- `CAIRN_final_cleaned.csv`

---

### 2. Articles_to_chunks.ipynb

**Purpose**  
Splitting articles into smaller text chunks suitable for downstream analyses (LDA, LLM).

**Input**
- `CAIRN_final_cleaned.csv`
- `LeMonde_auteur_filtré50.csv`

**Output**
- `CAIRN_clean_final_chunks.csv`
- `LM_real_final_chunks.csv`
- `CAIRN_chunks_and_authors.csv` (chunks with associated authors)

---

### 3. Basic_viz.ipynb

**Purpose**  
Basic descriptive visualizations for initial data exploration.

**Input**
- `LeMonde_auteur_filtré50.csv`
- `CAIRN_real_final.csv`

**Output**
- No output file generated

---

### 4. Lda_bootstrap.ipynb

**Purpose**  
Topic modeling using LDA with a bootstrap approach on Cairn article chunks.

**Input**
- `CAIRN_chunks_and_authors.csv`

**Output**
- `CAIRN_LDA_FINAL2.csv`

---

### 5. Reduction_CAIRN.ipynb

**Purpose**  
Reduction of CAIRN csv. with LDA results to make it exploitable by render.

**Input**
- `CAIRN_LDA_FINAL2.csv`

**Output**
- `CAIRN_LDA_LIGHT.csv`

---

### 6. Visualization_bootstrap.ipynb

**Purpose**  
Visualization of LDA bootstrap results.

**Input**
- `CAIRN_LDA_FINAL2.csv`

**Output**
- No output file generated

---

### 7. articles_random_selection.ipynb

**Purpose**  
Random selection of article chunks for manual inspection of LLM processing.

**Input**
- `CAIRN_real_final_chunks.csv`
- `LM_real_final_chunks.csv`

**Output**
- `sample_CAIRN_chunk.csv`
- `sample_LM_chunk.csv`

---

### 8. LLM.ipynb

**Purpose**  
Application of a Large Language Model on CAIRN and LeMonde articles.

**Input**
- `sample_CAIRN_chunk.csv`

**Output**
- `LLM_sample_chunk_CAIRN.csv`
- `LLM_sample_chunk_LM.csv`

---

### 9. Topics_to_json.ipynb

**Purpose**  
Conversion of textual topic descriptions into a JSON structure.

**Input**
- Text entry (manual input in notebook)

**Output**
- `topics_data.json`
