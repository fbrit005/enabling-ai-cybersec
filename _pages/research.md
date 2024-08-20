---
title: "Research"
layout: gridlay
sitemap: false
permalink: /research/
---

<style>
img{
  border-radius: 10px;
}
.col-md-3 {
  margin-top:10px;
  margin-bottom:10px;
  padding:0px;
  display:block;
  overflow:hidden;
  text-align:center;
  display: table-cell;
  background: white;
  border-radius: 20px;
  height: auto;
}
iframe {
  margin:0;
  padding:0;
  width: 175px;
  display: inline;
  vertical-align: middle;
}
</style>

# Research


<div class="jumbotron">
<div class="col-md-12 col-sm-12">
<h4>[Data Collection](data-collection)</h4>

For our data collection, we gathered over 5000 cybersecurity research papers from top cybersecurity conferences and journals (e.g., NDSS, USENIX, ACM CCS, and IEEE S&P). We gathered papers concerning computer security topics. After we collected our raw data, we adjusted a pre-trained model to filter the papers that have a higher probability of using AI topics. We then divide the papers into three distinct categories: AI-positive, AI-neutral, and AI-negative. For our analysis and results, we only considered the AI-positive papers.
</div>
</div>

<div class="jumbotron">
<div class="col-md-12 col-sm-12">
<h4>[Analysis](analysis)</h4>

## Setup Instructions
**1. Install all packages and download any commented sections.**

```bash
pip install -r requirements.txt
@@ -28,4 +35,4 @@ Run algorithm_lda script.
python algorithm_lda/algorithm_lda.py
```

**2. Read README.txt and run the executables.**

```bash
1. ai_parser.py
2. ai_cleaner.py
3. algorithm_lda.py
```

## Reproducibility Instructions
Our code includes the raw data used for reproducibility under the papers folder. To reproduce our results, please use our collection of research papers. Otherwise, feel free to use your own collection of papers.

1. [AI Parser](https://github.com/cslfiu/NSF_EAGER_SaTC_Project/blob/1c41fd26537495199317ab03d1dde6ebb8e4a229/ai_parser.py): This script code processes the PDF files into plaintext RAW files.
2. [AI Cleaner](https://github.com/cslfiu/NSF_EAGER_SaTC_Project/blob/1c41fd26537495199317ab03d1dde6ebb8e4a229/ai_cleaner.py): This script cleans the RAW files by removing stopwords and unnecessary data. It then exports CLEAN files.
3. [AI Helper](https://github.com/cslfiu/NSF_EAGER_SaTC_Project/blob/1c41fd26537495199317ab03d1dde6ebb8e4a229/ai_helper.py): This code contains helper methods used by the main and processor scripts.
4. [AI Check](https://github.com/cslfiu/NSF_EAGER_SaTC_Project/blob/1c41fd26537495199317ab03d1dde6ebb8e4a229/ai_check.py): This code uses an API key to check if a text is related to AI.
5. [AI Terms](https://github.com/cslfiu/NSF_EAGER_SaTC_Project/blob/1c41fd26537495199317ab03d1dde6ebb8e4a229/ai_terms.py): This code contains several lists consisting of AI and cybersecurity terms.
6. [Latent Dirichlet Algorithm (LDA)](https://github.com/cslfiu/NSF_EAGER_SaTC_Project/blob/1c41fd26537495199317ab03d1dde6ebb8e4a229/algorithm_lda/algorithm_lda.py): This analysis reads the CLEAN files to check if they contain AI terms. If a CLEAN file contains AI terms, the algorithm counts the number of AI and cybersecurity keywords and exports them into an Excel file. 


Once the analysis is complete, an Excel file will be created named "Results.xlsx." The files contain a list of documents containing machine learning-related terms after analysis is complete and the machine learning term used in the paper.

</div>
</div>
