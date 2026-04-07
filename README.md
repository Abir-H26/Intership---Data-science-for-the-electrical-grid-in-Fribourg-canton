<h1>Grid Infrastructure reliability &amp; Failure prediction (Groupe E Internship)</h1>

<h2>Overview</h2>
<p>
This project was completed during my internship at <strong>Groupe E</strong>, a major Swiss energy provider responsible for the operation and maintenance of low, medium, and high-voltage electrical networks.
The objective was to analyze historical equipment failures, understand their root causes, and build <strong>predictive reliability models</strong> using <strong>Weibull distributions</strong> to estimate future failure probabilities.
</p>
<p>
The work combines <strong>data science</strong>, <strong>power systems engineering</strong>, <strong>statistical reliability analysis</strong>, and <strong>natural language processing (NLP)</strong> for extracting structured insights from unstructured failure descriptions.
</p>

<pre><code>┌──────────────────────────────────────────────────────────┐
│        GRID INFRASTRUCTURE RELIABILITY PROJECT           │
├──────────────────────────────────────────────────────────┤
│  Historical Data (Structured + Text)                     │
│     • Equipment metadata                                  │
│     • Failure timestamps                                  │
│     • Maintenance logs                                    │
│     • Free‑text failure descriptions                      │
├──────────────────────────────────────────────────────────┤
│  Data Processing                                          │
│     • Cleaning &amp; standardization                         │
│     • Text preprocessing (NLP)                            │
│     • LLM-based semantic tagging                          │
│     • Time-to-failure computation                         │
├──────────────────────────────────────────────────────────┤
│  Analysis                                                 │
│     • EDA (patterns, trends, clusters)                    │
│     • Text mining (topics, keywords, modes)               │
│     • Weibull reliability modeling                        │
├──────────────────────────────────────────────────────────┤
│  Outputs                                                  │
│     • Hazard curves                                       │
│     • Remaining Useful Life (RUL) estimation              │
│     • Failure mode classification                         │
│     • Maintenance &amp; renewal insights                     │
└──────────────────────────────────────────────────────────┘</code></pre>


<h2>Confidentiality Notice</h2>
<p>
Due to contractual and operational confidentiality requirements at Groupe E:
</p>
<ul>
<li><strong>The original datasets cannot be shared.</strong></li>
<li><strong>The exact production code developed during the internship cannot be published.</strong></li>
</ul>
<p>
This README focuses on the conceptual framework, analytical approach, and insights that can be publicly disclosed.
</p>

<h2>Objectives</h2>
<ul>
<li><strong>Data consolidation:</strong> Merge and preprocess historical failure records from multiple internal sources.</li>
<li><strong>Context understanding:</strong> Analyze the operational role of low-, medium-, and high-voltage equipment.</li>
<li><strong>Failure analysis:</strong> Identify patterns, trends, and root causes of past failures.</li>
<li><strong>Text mining:</strong> Use NLP and LLM-based methods to classify and interpret free‑text failure descriptions.</li>
<li><strong>Reliability modeling:</strong> Build Weibull-based models to estimate failure rates, hazard functions, and remaining useful life (RUL).</li>
<li><strong>Decision support:</strong> Provide insights for maintenance optimization and asset renewal planning.</li>
</ul>

<h2>Data Description (Example)</h2>
<p>
The original dataset included operational and maintenance information for equipment across the grid. The synthetic data in this repository mimics:
</p>
<ul>
<li>Installation dates</li>
<li>Failure timestamps</li>
<li>Equipment categories (LV, MV, HV)</li>
<li>Environmental and operational metadata</li>
<li>Maintenance logs and <strong>free‑text failure descriptions</strong></li>
</ul>

<table>
<thead>
<tr>
<th>Voltage Level</th>
<th>Typical Equipment</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Low Voltage (LV)</strong></td>
<td>Cables, distribution boxes</td>
<td>High frequency of minor failures</td>
</tr>
<tr>
<td><strong>Medium Voltage (MV)</strong></td>
<td>Transformers, switchgear</td>
<td>Strong aging patterns</td>
</tr>
<tr>
<td><strong>High Voltage (HV)</strong></td>
<td>Transmission lines, substations</td>
<td>Low frequency, high impact</td>
</tr>
</tbody>
</table>

<h2>Methodology</h2>

<pre><code>Raw Data
   │
   ▼
┌────────────────────────────┐
│ Data Cleaning              │
│ • Remove duplicates        │
│ • Fix timestamps           │
│ • Standardize categories   │
└────────────────────────────┘
   │
   ├───────────────► Text Fields (Descriptions)
   │                     │
   │                     ▼
   │         ┌────────────────────────────┐
   │         │ NLP + LLM Processing       │
   │         │ • Tokenization             │
   │         │ • Keyword extraction       │
   │         │ • Semantic clustering      │
   │         │ • Failure mode tagging     │
   │         └────────────────────────────┘
   │
   ▼
┌────────────────────────────┐
│ Structured Dataset          │
│ (with enriched labels)      │
└────────────────────────────┘
   │
   ▼
┌────────────────────────────┐
│ Reliability Modeling        │
│ • Weibull fit               │
│ • Hazard function           │
│ • RUL estimation            │
└────────────────────────────┘
   │
   ▼
Insights &amp; Dashboards</code></pre>


<h3>1. Data Cleaning &amp; Preprocessing</h3>
<ul>
<li>Standardized equipment categories and voltage levels.</li>
<li>Removed duplicates and inconsistent timestamps.</li>
<li>Handled right-censored data (assets still in service).</li>
<li>Computed time-to-failure for each asset.</li>
<li>Processed unstructured text fields describing failures.</li>
</ul>

<h3>2. Exploratory Data Analysis</h3>
<ul>
<li>Failure frequency by voltage level and equipment type.</li>
<li>Age distribution and degradation patterns.</li>
<li>Seasonal and environmental correlations.</li>
<li>Detection of outliers and abnormal failure clusters.</li>
<li>Keyword and topic patterns extracted from text descriptions.</li>
</ul>

<h3>3. NLP &amp; LLM-Based Text Analysis</h3>

<pre><code>Free‑Text Failure Descriptions
                │
                ▼
     ┌──────────────────────┐
     │ Text Preprocessing   │
     │ • Cleaning           │
     │ • Lemmatization      │
     │ • Stopword removal   │
     └──────────────────────┘
                │
                ▼
     ┌──────────────────────┐
     │ Feature Extraction    │
     │ • Keywords            │
     │ • Embeddings          │
     │ • TF‑IDF / vectors    │
     └──────────────────────┘
                │
                ▼
     ┌──────────────────────┐
     │ LLM Semantic Layer    │
     │ • Classification      │
     │ • Mode tagging        │
     │ • Root cause mapping  │
     └──────────────────────┘
                │
                ▼
     ┌──────────────────────┐
     │ Structured Labels     │
     │ • Failure type        │
     │ • Severity            │
     │ • Cause category      │
     └──────────────────────┘</code></pre>


<p>
Many failure records included free‑text descriptions written by field technicians. To extract structured insights, I applied a combination of <strong>NLP preprocessing</strong> and <strong>LLM-assisted classification</strong>:
</p>
<ul>
<li>Tokenization, lemmatization, and stopword filtering.</li>
<li>Keyword extraction to identify recurring failure modes.</li>
<li>Clustering of descriptions to detect hidden categories.</li>
<li>LLM-based semantic classification to map text to standardized failure types.</li>
<li>Automatic tagging of root causes (e.g., insulation breakdown, moisture ingress, mechanical wear).</li>
</ul>
<p>
These techniques significantly improved the quality of the reliability models by enriching the dataset with <strong>consistent, machine-readable failure labels</strong>.
</p>

<h3>4. Weibull Reliability Modeling</h3>

<pre><code>Time-to-Failure Data
        │
        ▼
┌────────────────────────────┐
│ Weibull Fit                │
│ • Estimate β (shape)       │
│ • Estimate η (scale)       │
└────────────────────────────┘
        │
        ▼
┌────────────────────────────┐
│ Reliability Outputs         │
│ • PDF / CDF                 │
│ • Hazard function h(t)      │
│ • Survival function S(t)    │
│ • RUL distribution          │
└────────────────────────────┘
        │
        ▼
Maintenance &amp; Renewal Strategy</code></pre>


<p>
Weibull analysis was used to model time-to-failure:
</p>
<p>
f(t) = (β / η) · (t / η)<sup>β - 1</sup> · exp(-(t / η)<sup>β</sup>)
</p>
<ul>
<li><strong>β (shape parameter):</strong> characterizes the failure mode.</li>
<li><strong>η (scale parameter):</strong> characteristic life.</li>
</ul>
<p>
Interpretation:
</p>
<ul>
<li>β &lt; 1: early-life failures.</li>
<li>β = 1: random failures.</li>
<li>β &gt; 1: wear-out failures.</li>
</ul>

<h3>5. Predictive Insights</h3>
<ul>
<li>Estimated hazard curves for each voltage level and equipment family.</li>
<li>Computed remaining useful life distributions.</li>
<li>Identified aging equipment entering the wear-out phase.</li>
<li>Supported prioritization of maintenance and replacement strategies.</li>
<li>Linked text-derived failure modes to reliability patterns.</li>
</ul>

<pre><code>┌──────────────────────────────────────────────────────────────────────────┐
│                         END‑TO‑END WORKFLOW                              │
├──────────────────────────────────────────────────────────────────────────┤
│ 1. Data Sources                                                           │
│    • Equipment metadata                                                   │
│    • Failure logs                                                         │
│    • Technician text descriptions                                         │
├──────────────────────────────────────────────────────────────────────────┤
│ 2. Preprocessing                                                          │
│    • Cleaning + standardization                                           │
│    • Time-to-failure computation                                          │
│    • NLP preprocessing of text                                            │
├──────────────────────────────────────────────────────────────────────────┤
│ 3. NLP &amp; LLM Analysis                                                     │
│    • Keyword extraction                                                   │
│    • Topic clustering                                                     │
│    • Semantic classification (LLM)                                        │
│    • Failure mode tagging                                                 │
├──────────────────────────────────────────────────────────────────────────┤
│ 4. Reliability Modeling                                                   │
│    • Weibull fit                                                          │
│    • Hazard curves                                                        │
│    • RUL estimation                                                       │
├──────────────────────────────────────────────────────────────────────────┤
│ 5. Decision Support                                                       │
│    • Maintenance prioritization                                           │
│    • Asset renewal planning                                               │
│    • Long-term failure forecasting                                        │
└──────────────────────────────────────────────────────────────────────────┘</code></pre>


<h2>Key Results (High-Level Summary)</h2>
<ul>
  <li><strong>Identified reliability profiles</strong> for LV, MV, and HV equipment families, revealing distinct aging behaviors and failure dynamics across the grid.</li>
  <li><strong>Extracted structured failure modes</strong> from technician reports using NLP and LLM-based semantic tagging, reducing ambiguity in historical records.</li>
  <li><strong>Built Weibull models</strong> that captured wear-out patterns in MV assets (β &gt; 1) and confirmed random failure behavior in LV components (β ≈ 1).</li>
  <li><strong>Generated hazard curves</strong> and <strong>Remaining Useful Life (RUL)</strong> estimates enabling medium- and long-term forecasts (5–30 years).</li>
  <li><strong>Linked text-derived failure modes to statistical patterns</strong>, improving interpretability of reliability trends and supporting root-cause analysis.</li>
  <li><strong>Provided actionable insights</strong> for maintenance prioritization, asset renewal planning, and long-term investment strategies.</li>
</ul>


<h2>My Achievements During the Internship</h2>
<ul>
  <li><strong>Designed and implemented</strong> an end-to-end reliability analysis pipeline, from raw data ingestion to Weibull-based forecasting.</li>
  <li><strong>Developed NLP and LLM-powered tools</strong> to interpret unstructured technician failure descriptions, enabling consistent failure mode classification across asset families.</li>
  <li><strong>Consolidated and cleaned heterogeneous datasets</strong>, correcting approximately <strong>30%</strong> of inconsistent or incomplete records and standardizing equipment metadata.</li>
  <li><strong>Analyzed reliability behavior</strong> across more than five equipment categories spanning low-, medium-, and high-voltage networks.</li>
  <li><strong>Built and validated Weibull models</strong> for multiple asset families, producing hazard curves, survival functions, and RUL distributions used by asset managers.</li>
  <li><strong>Created interactive dashboards and visual analytics</strong> to communicate reliability trends and support operational decision-making.</li>
  <li><strong>Collaborated with engineers and analysts</strong> to interpret results, validate assumptions, and integrate domain knowledge into the modeling process.</li>
  <li><strong>Documented the full methodology</strong> to ensure reproducibility and facilitate future integration into Groupe E’s internal tools.</li>
</ul>


<h2>Tools &amp; Technologies</h2>

<h3>1. Data Processing &amp; Analysis</h3>
<ul>
  <li><strong>pandas</strong> — data cleaning, merging, preprocessing</li>
  <li><strong>numpy</strong> — numerical computations</li>
  <li><strong>scipy</strong> — statistical functions and optimization</li>
</ul>

<h3>2. Reliability Engineering</h3>
<ul>
  <li><strong>reliability</strong> — Weibull fitting, hazard curves, survival analysis, RUL estimation</li>
  <li><strong>matplotlib</strong> — reliability curve visualization</li>
  <li><strong>seaborn</strong> — statistical plotting and EDA visuals</li>
</ul>

<h3>3. NLP &amp; LLM-Based Text Analysis</h3>
<ul>
  <li><strong>spaCy</strong> — tokenization, lemmatization, linguistic preprocessing</li>
  <li><strong>scikit-learn</strong> — TF-IDF, clustering, keyword extraction</li>
  <li><strong>transformers</strong> (HuggingFace) — LLM-based semantic classification</li>
  <li><strong>sentence-transformers</strong> — high-quality text embeddings for semantic similarity</li>
</ul>

<h3>4. Development &amp; Documentation</h3>
<ul>
  <li><strong>Jupyter Notebook / JupyterLab</strong> — interactive analysis and reporting</li>
  <li><strong>tqdm</strong> — progress bars for long-running preprocessing tasks</li>
  <li><strong>json / pyyaml</strong> — configuration and metadata handling</li>
</ul>

<h2>What I Learned</h2>
<ul>
  <li>Applying statistical reliability models to real-world grid infrastructure and interpreting their operational impact.</li>
  <li>Designing robust preprocessing workflows to handle imperfect industrial datasets with missing or inconsistent information.</li>
  <li>Using NLP and LLM-based techniques to extract structured insights from unstructured technician failure descriptions.</li>
  <li>Connecting engineering intuition with data-driven evidence to support maintenance and asset-renewal decisions.</li>
  <li>Communicating complex reliability concepts—such as hazard rates, Weibull parameters, and RUL—to both technical and non-technical stakeholders.</li>
  <li>Bridging electrical engineering, data science, and text analytics within a unified analytical pipeline.</li>
</ul>

