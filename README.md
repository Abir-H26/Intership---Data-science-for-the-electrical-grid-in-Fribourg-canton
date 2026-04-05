<h1>Grid Infrastructure Reliability &amp; Failure Prediction (Groupe E Internship)</h1>

<h2>Overview</h2>
<p>
  This project was completed during my internship at <strong>Groupe E</strong>, a major Swiss energy provider responsible for the operation and maintenance of low-, medium-, and high-voltage electrical networks.
  The objective was to analyze historical equipment failures, understand their root causes, and build <strong>predictive reliability models</strong> using <strong>Weibull distributions</strong> to estimate future failure probabilities.
</p>
<p>
  The work combines <strong>data science</strong>, <strong>power systems engineering</strong>, and <strong>statistical reliability analysis</strong>, supporting long-term asset management and maintenance planning.
</p>

<h2>Confidentiality Notice</h2>
<p>
  Due to contractual and operational confidentiality requirements at Groupe E:
</p>
<ul>
  <li><strong>The original datasets cannot be shared.</strong></li>
  <li><strong>The exact production code developed during the internship cannot be published.</strong></li>
</ul>
<p>
  All examples in this repository use <strong>synthetic or anonymized data</strong>, and the code reflects the <strong>general methodology</strong>, not the internal implementation.
  This README focuses on the conceptual framework, analytical approach, and insights that can be publicly disclosed.
</p>

<h2>Objectives</h2>
<ul>
  <li><strong>Data consolidation:</strong> Merge and preprocess historical failure records from multiple internal sources.</li>
  <li><strong>Context understanding:</strong> Analyze the operational role of low-, medium-, and high-voltage equipment.</li>
  <li><strong>Failure analysis:</strong> Identify patterns, trends, and root causes of past failures.</li>
  <li><strong>Reliability modeling:</strong> Build Weibull-based models to estimate failure rates, hazard functions, and remaining useful life (RUL).</li>
  <li><strong>Decision support:</strong> Provide insights for maintenance optimization and asset renewal planning.</li>
</ul>

<h2>Data Description (Synthetic Example)</h2>
<p>
  The original dataset included operational and maintenance information for equipment across the grid. The synthetic data in this repository mimics:
</p>
<ul>
  <li>Installation dates</li>
  <li>Failure timestamps</li>
  <li>Equipment categories (LV, MV, HV)</li>
  <li>Environmental and operational metadata</li>
  <li>Maintenance logs</li>
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

<h3>1. Data Cleaning &amp; Preprocessing</h3>
<ul>
  <li>Standardized equipment categories and voltage levels.</li>
  <li>Removed duplicates and inconsistent timestamps.</li>
  <li>Handled right-censored data (assets still in service).</li>
  <li>Computed time-to-failure for each asset.</li>
</ul>

<h3>2. Exploratory Data Analysis</h3>
<ul>
  <li>Failure frequency by voltage level and equipment type.</li>
  <li>Age distribution and degradation patterns.</li>
  <li>Seasonal and environmental correlations.</li>
  <li>Detection of outliers and abnormal failure clusters.</li>
</ul>

<h3>3. Weibull Reliability Modeling</h3>
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

<h3>4. Predictive Insights</h3>
<ul>
  <li>Estimated hazard curves for each voltage level and equipment family.</li>
  <li>Computed remaining useful life distributions.</li>
  <li>Identified aging equipment entering the wear-out phase.</li>
  <li>Supported prioritization of maintenance and replacement strategies.</li>
</ul>

<h2>Key Results (High-Level Summary)</h2>
<ul>
  <li><strong>LV equipment:</strong> high failure count, mostly random behavior (β ≈ 1).</li>
  <li><strong>MV equipment:</strong> clear wear-out patterns (β &gt; 1), indicating aging infrastructure.</li>
  <li><strong>HV equipment:</strong> rare failures but strongly age-dependent.</li>
  <li>Weibull models enabled medium- to long-term forecasts (5–20 years) of failure probabilities.</li>
</ul>

<h2>My Achievements During the Internship</h2>
<ul>
  <li><strong>Developed</strong> a complete reliability analysis workflow using Python, from data cleaning to Weibull modeling.</li>
  <li><strong>Analyzed</strong> over <strong>5</strong> equipment categories across low-, medium-, and high-voltage networks.</li>
  <li><strong>Built</strong> Weibull models for <strong>5</strong> asset families to estimate failure rates and remaining useful life.</li>
  <li><strong>Improved</strong> data quality by identifying and correcting the <strong>30%</strong> inconsistent or missing records.</li>
  <li><strong>Created</strong> visual dashboards and reliability curves used by the asset management team.</li>
  <li><strong>Delivered</strong> a predictive framework capable of forecasting failures over the next <strong>30</strong> years.</li>
  <li><strong>Collaborated</strong> with engineers and data analysts to interpret results and support maintenance planning.</li>
  <li><strong>Documented</strong> the entire methodology to ensure reproducibility and future integration into internal tools.</li>
</ul>


<h2>Tools &amp; Technologies</h2>
<ul>
  <li><strong>Python:</strong> pandas, numpy, scipy, matplotlib, seaborn</li>
  <li><strong>Reliability interface:</strong> reliability</li>
  <li><strong>Jupyter Notebooks</strong> for analysis and visualization</li>
  <li>Domain knowledge in <strong>power systems</strong> and <strong>equipment aging</strong></li>
</ul>

<h2>What I Learned</h2>
<ul>
  <li>Applying statistical reliability models to real-world grid infrastructure.</li>
  <li>Handling imperfect industrial datasets and need to cope for lack of informations.</li>
  <li>Translating engineering intuition into data-driven insights.</li>
  <li>Communicating results to both technical and non-technical stakeholders.</li>
  <li>Bridging electrical engineering and data science in an operational context.</li>
</ul>
