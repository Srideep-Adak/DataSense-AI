<div align="center">

# 📊 DataSense

### *Ask Data. Get Answers. No Code.*

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![LangChain](https://img.shields.io/badge/LangChain-Core-green.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-App-red.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

**DataSense** is an AI-powered natural-language data analysis assistant that transforms your datasets into meaningful insights, visualizations, and actionable answers — without requiring you to write code.

</div>

---

## 📌 Overview

**DataSense** is a Streamlit-based data analysis platform that allows users to interact with CSV and Excel datasets using **natural language**.

Instead of writing Python or SQL queries, users can simply upload their data and ask questions such as:

> *"What is the average revenue by country?"*

> *"Show me the top 10 products by sales."*

> *"Create a line chart showing monthly revenue."*

DataSense uses AI models to understand the user's request, perform the required data analysis, and present the results through **tables, statistics, and visualizations**.

---

## ✨ Key Features

### 📈 1. Automated Exploratory Data Analysis

Get an instant overview of your dataset without manually performing EDA.

**Features include:**

* Total rows and columns
* Duplicate row detection
* Missing-value analysis
* Data type information
* Unique-value statistics
* Interactive data preview
* Numerical statistical summaries
* Mean, median, quartiles, and standard deviation
* Outlier analysis
* Correlation matrix
* Categorical value distributions
* Missing-value visualizations
* Exportable EDA reports

---

### 💬 2. Natural Language Query

Interact with your dataset using plain English.

DataSense converts natural-language questions into data operations and returns results based on the actual dataset.

**Example queries:**

```text
What is the average age of customers?
```

```text
Show me the top 5 countries by total revenue.
```

```text
How has sales changed year-over-year?
```

```text
What percentage of orders have missing customer information?
```

**Capabilities:**

* Filtering
* Grouping
* Aggregation
* Sorting
* Statistical calculations
* Multi-step data analysis
* Real-time computed results
* AI-generated query suggestions

---

### 📊 3. AI-Powered Visualization

Generate charts simply by describing what you want.

For example:

```text
Create a bar chart showing the top 10 countries by revenue.
```

DataSense generates the required visualization code and displays the resulting chart.

**Supported visualizations include:**

* Bar charts
* Line charts
* Scatter plots
* Histograms
* Box plots
* Heatmaps
* Distribution plots
* Comparative charts

Additional features include:

* AI-generated visualization suggestions
* Automatic chart generation
* Generated-code preview
* Interactive visualization workflow

---

### 🔧 4. AI Dataframe Manipulation

Clean and transform datasets using natural-language instructions.

For example:

```text
Remove rows where the email column is missing.
```

or:

```text
Keep only name, age, and salary columns and sort by salary descending.
```

DataSense generates the corresponding Pandas operations and allows users to preview the changes before applying them.

**Features:**

* Natural-language transformations
* Column selection
* Filtering
* Sorting
* Grouping
* Missing-value handling
* Data cleaning
* Preview before applying changes
* Download transformed datasets
* Generated-code transparency

---

### 🔐 5. Safe Code Execution

Since DataSense generates and executes code dynamically, security is an important part of the application.

The platform includes execution guardrails designed to:

* Restrict potentially dangerous operations
* Control generated code execution
* Reduce unintended system access
* Keep data-analysis operations focused on the uploaded dataset

---

## 🧠 How DataSense Works

```text
             ┌──────────────────┐
             │   Upload Dataset │
             │   CSV / Excel    │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │  Data Processing │
             │   & Validation   │
             └────────┬─────────┘
                      │
          ┌───────────┼───────────┐
          │           │           │
          ▼           ▼           ▼
       ┌──────┐   ┌───────┐   ┌──────────┐
       │ EDA  │   │  NLQ  │   │   Data   │
       │      │   │       │   │Manipulation│
       └──┬───┘   └───┬───┘   └─────┬────┘
          │           │              │
          └───────────┼──────────────┘
                      ▼
             ┌──────────────────┐
             │    AI Model      │
             │ Gemini / GPT /   │
             │ Claude           │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Results &        │
             │ Visualizations   │
             └──────────────────┘
```

---

## 🤖 Supported AI Models

DataSense supports multiple AI providers, allowing users to choose the model that best fits their requirements.

| Provider      | Example Model              | Primary Use                   |
| ------------- | -------------------------- | ----------------------------- |
| Google Gemini | `gemini-2.5-flash`         | Fast general-purpose analysis |
| OpenAI        | `gpt-4o-mini`              | Balanced performance and cost |
| Anthropic     | `claude-3-5-sonnet-latest` | Complex reasoning             |

### Model Flexibility

Compatible models can be configured according to the selected provider.

**OpenAI examples:**

* GPT-4
* GPT-4 Turbo
* GPT-4o Mini

**Google examples:**

* Gemini 2.5 Flash
* Gemini 2.5 Pro

**Anthropic examples:**

* Claude Sonnet
* Claude Opus

---

## 🛠️ Technology Stack

| Technology           | Purpose                      |
| -------------------- | ---------------------------- |
| **Python**           | Core application development |
| **Streamlit**        | Web application interface    |
| **Pandas**           | Data processing and analysis |
| **Matplotlib**       | Data visualization           |
| **Seaborn**          | Statistical visualization    |
| **LangChain**        | AI and agent integration     |
| **OpenAI**           | LLM-powered analysis         |
| **Google Gemini**    | LLM-powered analysis         |
| **Anthropic Claude** | LLM-powered analysis         |

---

## 📁 Project Structure

```text
DataSense/
│
├── app.py
├── requirements.txt
├── README.md
├── LICENSE
├── favicon.svg
│
├── utils/
│   ├── __init__.py
│   ├── model.py
│   ├── io_utils.py
│   ├── eda.py
│   ├── suggestions.py
│   ├── nlq.py
│   ├── viz.py
│   └── df_manip.py
│
└── test_utils/
    ├── EDA.py
    ├── NLQ.py
    ├── Visualization.ipynb
    ├── Insight_suggestor.py
    └── dataframe_manipulation.py
```

### Main Components

* **`app.py`** — Main Streamlit application
* **`model.py`** — AI model initialization and configuration
* **`io_utils.py`** — CSV and Excel file handling
* **`eda.py`** — Exploratory data analysis
* **`suggestions.py`** — AI-generated analytical suggestions
* **`nlq.py`** — Natural-language query processing
* **`viz.py`** — AI-powered visualization generation
* **`df_manip.py`** — AI-assisted dataframe transformation

---

## 📂 Supported File Formats

DataSense currently supports:

* `.csv`
* `.xlsx`
* `.xls`

### Recommended Dataset Size

Datasets up to approximately **200 MB** are recommended for smooth operation.

> Performance may vary depending on dataset size, complexity, available system resources, and the selected AI model.

For Excel workbooks containing multiple sheets, the application currently processes the first sheet.

---

## 🚀 Installation

### Prerequisites

Make sure the following are installed:

* Python **3.10 or higher**
* pip
* An API key from at least one supported AI provider

---

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/DataSense.git
cd DataSense
```

---

### 2. Create a Virtual Environment

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Configure API Keys

Configure the API key for your selected AI provider.

Supported providers include:

* OpenAI
* Google Gemini
* Anthropic Claude

Keep API keys private and avoid committing them to GitHub.

---

### 5. Run DataSense

```bash
streamlit run app.py
```

The application will start locally and can be accessed through the URL provided by Streamlit, typically:

```text
http://localhost:8501
```

---

## 💡 Example Use Cases

### 🏢 Business Analytics

* Analyze sales performance
* Compare regional revenue
* Identify business trends
* Explore customer behavior
* Generate management-ready visualizations

### 🧑‍💻 Data Science

* Perform rapid exploratory data analysis
* Identify correlations
* Analyze distributions
* Explore datasets before modeling
* Generate visualizations quickly

### 🔬 Research

* Analyze survey datasets
* Explore experimental results
* Identify patterns and relationships
* Generate statistical summaries
* Create research visualizations

### 📊 Data Exploration

* Ask questions about unfamiliar datasets
* Find trends and anomalies
* Clean datasets using natural language
* Transform data without writing Pandas code

---

## 🔒 Security & Privacy

DataSense is designed with security considerations for AI-generated code execution.

Users should:

* Never expose API keys publicly
* Avoid uploading confidential data to third-party AI providers unless appropriate permissions are in place
* Review generated code before executing transformations
* Use environment variables or secure configuration for API credentials

---

## 🗺️ Future Enhancements

Potential future improvements include:

* 📌 Support for larger datasets
* 📌 Interactive dashboard generation
* 📌 SQL database connectivity
* 📌 Advanced statistical analysis
* 📌 Automated insight generation
* 📌 PDF and Excel report generation
* 📌 Multi-dataset analysis
* 📌 Conversation history
* 📌 User authentication
* 📌 Cloud deployment
* 📌 Additional LLM providers

---

## 📄 License

This project is licensed under the **MIT License**.

See the `LICENSE` file for more information.

---

<div align="center">

### ⭐ DataSense

**Ask Data. Get Answers. No Code.**

Made with ❤️ using Python, Streamlit, LangChain, and modern AI models.

</div>
