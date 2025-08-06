# Alteryx-Inspire-2022-PDFs
Presentation and workflows from my presentation at Inspire 2022
Gaining Insight from PDFs with Alteryx Intelligence Suite
INS‑302 Conference Session, Chris Goodman – PwC 

Overview
Critical business data often sits locked inside semi‑structured or unstructured PDF files—supplier invoices, financial statements, lengthy strategic reports, and more. This repository accompanies the INS‑302 presentation and walks you through using Alteryx Intelligence Suite to unlock that information and feed it straight into your analytics pipeline. 

You will learn how to …
Extract Key‑Value Pairs (KVP) that appear in different positions across multiple document templates.

Recognise Named Entities (NER)—companies, people, locations—directly from PDF text.

Leverage Annotation for PDFs that follow a rigid layout.

Apply Topic Modelling to large corpora (e.g., FTSE‑350 strategic reports) and surface emergent themes such as COVID‑19 vs pandemic without exhaustive keyword lists. 

Repository Contents
bash
Copy
.
├── data/                 # Sample PDFs: invoices, real‑estate summaries, FTSE‑350 reports
├── workflows/            # Alteryx .yxmd / .yxzp workflows built in the session
├── models/               # Trained KVP & NER models
├── notebooks/            # Optional Python notebooks for post‑processing
├── docs/
│   └── presentation.pdf  # Slide deck export
└── README.md             # <— you are here
Quick Start
bash
Copy
# 1  Clone the repository
git clone https://github.com/<your‑org>/pdf‑insight‑intelligence‑suite.git
cd pdf‑insight‑intelligence‑suite

# 2  Open Alteryx Designer 2022.1+ with an Intelligence Suite licence
# 3  Import the packaged workflow
AlteryxDesignerCmd.exe /open workflows/INS‑302‑demo.yxzp
Then run the workflows in order:

Workflow	Purpose
1_annotation_example.yxmd	Capture tabular data from fixed‑layout property summaries
2_kvp_invoices.yxmd	Detect Invoice Number, Supplier, Total, etc., across many invoice styles
3_ner_financials.yxmd	Enrich annual reports with named entities for downstream analysis
4_topic_modelling_ftse350.yxmd	Cluster FTSE‑350 strategic reports into thematic groups

Tip: Each workflow contains a Control Parameter so you can swap in your own PDFs without editing the underlying logic.

Prerequisites
Requirement	Minimum Version
Alteryx Designer + Intelligence Suite	2022.1
PDFium or Ghostscript (optional)	Latest
Python (for notebooks)	3.8

Extending the Project
Add more document templates and retrain the KVP model to improve recall.

Adjust Topic Modelling parameters (e.g., number of topics) to fine‑tune clustering.

Chain outputs into predictive, geospatial, or reporting workflows for deeper insight.

Slides
A PDF export of the original conference deck is available under docs/presentation.pdf; the source PowerPoint is included for speaker notes and animations. 

Credits
Chris Goodman, PwC – original author of the INS‑302 session

Alteryx Product Engineering – Intelligence Suite tooling

Sample documents are anonymised and provided for demonstration only

License
Released under the MIT License. See LICENSE for details.
