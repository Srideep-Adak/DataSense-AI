<div align="center">

# 📊 DataSense-AI

### *Ask Data. Get Answers. No Code.*

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![LangChain](https://img.shields.io/badge/LangChain-Core-green.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-App-red.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

**DataSense-AI** is an AI-powered natural-language data analysis assistant that transforms datasets into meaningful insights, visualizations, and actionable answers — without requiring users to write code.

**Developed by Srideep Adak**

</div>

---

## 🎯 Overview

**DataSense-AI** is a Streamlit-based intelligent data analysis platform that allows users to interact with **CSV and Excel datasets using natural language**.

Instead of writing Python or SQL queries, users can simply upload their dataset and ask questions such as:

> *"What is the average revenue by country?"*

> *"Show me the top 10 products by sales."*

> *"Create a line chart showing monthly revenue."*

DataSense-AI uses Large Language Models (LLMs) to understand user requests, perform data analysis, generate visualizations, and provide meaningful insights.

---

## ✨ Features

### 📈 1. Automated Exploratory Data Analysis

DataSense-AI automatically performs comprehensive EDA on uploaded datasets.

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

Interact with your dataset using plain English instead of writing code.

DataSense-AI processes natural-language questions and performs the required data operations on the uploaded dataset.

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

**Supported operations include:**

* Filtering
* Grouping
* Aggregation
* Sorting
* Statistical calculations
* Multi-step analysis
* AI-generated query suggestions

---

### 📊 3. AI-Powered Visualization

Generate visualizations simply by describing what you want.

For example:

```text
Create a bar chart showing the top 10 countries by revenue.
```

DataSense-AI generates the required visualization code and displays the resulting chart.

**Supported visualizations include:**

* Bar charts
* Line charts
* Scatter plots
* Histograms
* Box plots
* Heatmaps
* Distribution plots
* Comparative charts

Additional capabilities:

* AI-generated visualization suggestions
* Automatic chart generation
* Generated-code preview
* Natural-language chart descriptions

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

DataSense-AI generates the required Pandas operations and allows users to preview the changes before applying them.

**Features include:**

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

DataSense-AI includes security guardrails for AI-generated code execution.

The platform is designed to:

* Restrict potentially dangerous operations
* Control generated-code execution
* Reduce unintended system access
* Keep operations focused on the uploaded dataset

---

## 🧠 How DataSense-AI Works

```text
                 ┌─────────────────────┐
                 │    Upload Dataset   │
                 │     CSV / Excel     │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │  Data Processing &  │
                 │     Validation      │
                 └──────────┬──────────┘
                            │
              ┌─────────────┼─────────────┐
              │             │             │
              ▼             ▼             ▼
         ┌────────┐    ┌─────────┐   ┌──────────┐
         │  EDA   │    │   NLQ   │   │ Dataframe│
         │Analysis│    │ Queries │   │Manipulation│
         └───┬────┘    └────┬────┘   └─────┬────┘
             │              │              │
             └──────────────┼──────────────┘
                            ▼
                 ┌─────────────────────┐
                 │      AI / LLM       │
                 │ Gemini / GPT /      │
                 │ Claude              │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Results, Insights & │
                 │   Visualizations    │
                 └─────────────────────┘
```

---

## 🏗️ System Architecture

```text
User
 │
 ▼
Streamlit Web Interface
 │
 ├───────────────┬─────────────────┐
 ▼               ▼                 ▼
EDA Module    NLQ Module      Visualization
 │               │                 │
 └───────────────┼─────────────────┘
                 ▼
          LangChain Framework
                 │
       ┌─────────┼─────────┐
       ▼         ▼         ▼
    OpenAI    Gemini    Claude
       │         │         │
       └─────────┼─────────┘
                 ▼
          Pandas / Python
                 │
                 ▼
          Analysis Results
                 │
                 ▼
       Tables / Charts / Insights
```

---

## 🛠️ Technology Stack

| Technology           | Purpose                      |
| -------------------- | ---------------------------- |
| **Python**           | Core application development |
| **Streamlit**        | Interactive web interface    |
| **Pandas**           | Data processing and analysis |
| **Matplotlib**       | Data visualization           |
| **Seaborn**          | Statistical visualization    |
| **LangChain**        | LLM and agent integration    |
| **OpenAI**           | AI-powered analysis          |
| **Google Gemini**    | AI-powered analysis          |
| **Anthropic Claude** | AI-powered analysis          |

---

## 📁 Project Structure

```text
DataSense-AI/
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

| File             | Description                               |
| ---------------- | ----------------------------------------- |
| `app.py`         | Main Streamlit application                |
| `model.py`       | AI model initialization and configuration |
| `io_utils.py`    | CSV and Excel file handling               |
| `eda.py`         | Exploratory data analysis                 |
| `suggestions.py` | AI-generated analytical suggestions       |
| `nlq.py`         | Natural-language query processing         |
| `viz.py`         | AI-powered visualization generation       |
| `df_manip.py`    | AI-assisted dataframe transformation      |

---

## 🤖 Supported AI Models

DataSense-AI supports multiple AI providers.

| Provider         | Example Model              | Use Case                      |
| ---------------- | -------------------------- | ----------------------------- |
| Google Gemini    | `gemini-2.5-flash`         | Fast general-purpose analysis |
| OpenAI           | `gpt-4o-mini`              | Balanced performance and cost |
| Anthropic Claude | `claude-3-5-sonnet-latest` | Complex reasoning             |

The model can be configured according to the selected provider and application requirements.

---

## 📂 Supported File Formats

DataSense-AI supports:

* **CSV** — `.csv`
* **Excel** — `.xlsx`
* **Excel** — `.xls`

### Recommended Dataset Size

Datasets up to approximately **200 MB** are recommended for smooth operation.

Performance may vary depending on dataset size, complexity, available system resources, and the selected AI model.

For Excel workbooks containing multiple sheets, the application processes the first sheet.

---

## 🚀 Installation

### Prerequisites

Make sure you have:

* Python **3.10+**
* pip
* API key from at least one supported AI provider

---

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/DataSense-AI.git
cd DataSense-AI
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

Configure the API key for your preferred AI provider:

* OpenAI
* Google Gemini
* Anthropic Claude

**Important:** Never commit API keys directly to the repository.

---

### 5. Run the Application

```bash
streamlit run app.py
```

The application will typically be available at:

```text
http://localhost:8501
```

---

## 💡 Example Use Cases

### 🏢 Business Analytics

* Analyze sales performance
* Compare regional revenue
* Identify business trends
* Analyze customer behavior
* Generate business visualizations

### 🧑‍💻 Data Science

* Perform automated EDA
* Explore unfamiliar datasets
* Identify correlations
* Analyze distributions
* Generate visualizations
* Perform preliminary data analysis

### 🔬 Research

* Analyze survey datasets
* Explore experimental results
* Identify relationships between variables
* Generate statistical summaries
* Create research visualizations

### 📊 General Data Exploration

* Ask questions about datasets
* Discover trends and patterns
* Clean data using natural language
* Transform datasets without writing Pandas code

---

## 🔒 Security & Privacy

DataSense-AI is designed with security considerations for AI-generated code execution.

Users should:

* Keep API keys private
* Avoid uploading confidential data to third-party AI providers unless appropriate permissions are in place
* Review generated code before executing transformations
* Use environment variables or secure configuration for API credentials

---

## 🗺️ Future Enhancements

Planned or potential improvements include:

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

## 📊 DataSense-AI

### *Ask Data. Get Answers. No Code.*

**Developed by Srideep Adak**

Built with ❤️ using Python, Streamlit, LangChain, and modern AI models.

⭐ **Star this repository if you find it useful!**

</div>
