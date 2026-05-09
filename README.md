# ImmunoTwin-Sim-v2.0
ImmunoTwin-Sim is a high-performance in-silico simulation tool designed to identify drug repurposing candidates for rare and complex diseases. By utilizing a Reverse-Transcriptomics approach, the platform compares a patient’s disease-specific gene expression profile against a global database of drug-induced perturbation signatures.
The goal of this tool is to help researchers and clinicians identify existing FDA-approved drugs that can "flip" or "reverse" a disease's genetic signature back toward a healthy state.

🚀 Key Features
- Universal Discovery Engine: Powered by the Enrichr L1000 database, providing access to thousands of drug signatures.

- Fail-Safe Architecture: Combines a local high-speed knowledge base with a live API fallback for 100% stability.

- Multi-Domain Application: Successfully tested across Autoimmune (Dermatomyositis), Oncology (Neuroblastoma), and Neurology (Huntington’s Disease).

- Real-time Visualization: Interactive Plotly-based dashboards for calculating "Repurposing Potential" scores.

- Fuzzy Search Technology: Intelligent drug name matching to handle database naming variations.

🛠️ The Concept: Signature Reversal
- The core logic of ImmunoTwin-Sim follows a "Lock and Key" mechanism:

- The Lock (Disease Profile): Upregulated genes driving a rare disease.

- The Key (Drug Signature): Genes suppressed by a specific drug.

- The Match: The tool calculates the overlap.
If a drug's suppression signature targets the disease's driver genes, it has high repurposing potential.

📂 Installation & Usage
1. Prerequisites
Ensure you have Python installed, then install the required libraries:
pip install streamlit pandas requests plotly

2. Run the Application
streamlit run ImmunoTwin-Sim.py

3. How to Use
- Sidebar: Select a drug from the dropdown or type a custom name (e.g., Baricitinib, Anifrolumab).
Sidebar: Select or type the target disease (e.g., Dermatomyositis).

- Step 1: Upload a CSV file of the disease profile. The file must have a column named gene_symbol.

- Step 2: View the Repurposing Potential score and the specific molecular targets being reversed.

📊 Sample Test Data
To demonstrate universality, you can test the following pairs using data from NCBI GEO:

| Disease | GEO Accession | Recommended Test Drug |
| --- | --- | --- |
| **Dermatomyositis** | GSE142807 | Tofacitinib / Baricitinib |
| **Neuroblastoma** | GSE120572 | Vincristine |
| **Huntington’s Disease** | GSE3790 | Memantine |

🧬 Technology Stack
- Language: Python 3.x

- Frontend: Streamlit

- Data Analysis: Pandas, NumPy

- Visualization: Plotly Express
