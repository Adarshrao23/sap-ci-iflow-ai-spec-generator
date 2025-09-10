# SAP CI/CPI iFlow Technical Specification Generator using Generative AI

## 🚀 Overview

This project automates the creation of technical specification documents for SAP Integration Suite (CI/CPI) iFlows using Generative AI (Google Gemini). It parses iFlow XML files, extracts metadata and Groovy scripts, and generates a professional Word document with diagrams and AI-generated summaries.

## ✨ Features

- Parses iFlow `.iflw` XML files
- Uses Google Gemini API to generate human-readable summaries
- Creates structured Word documents with:
  - Overview
  - High-Level Design
  - Message Flow
  - Technical Description
  - Sender/Receiver Details
  - Mappings
  - Security & Error Handling
  - Appendix
- Visualizes BPMN flows using `matplotlib` and `networkx`
- Extracts and explains Groovy scripts
- Supports versioning and metadata

## 🛠️ Installation

To install the required software and clone the repository, run the following commands:

```
git clone https://github.com/AdarshRao23/sap-iflow-spec-generator.git
cd sap-iflow-spec-generator
```

## ⚙️ Configuration
Prepare a configuration file named config_file.json. This file should have the following structure:
```
{
  "gemini_api_key": "YOUR_API_KEY",
  "iflow_xml_path": "path/to/iflow.iflw",
  "groovy_scripts_path": "path/to/groovy/scripts",
  "output_doc_path": "output/specification.docx"
}
```
## ▶️ Usage
To generate the specification document, execute the following command:
python Dynamic_generate_iflow_spec_using_ai.py
### 💡 Usage Examples
#### Example 1: Basic iFlow Documentation
Result: 
A Word document featuring:

- Overview of the Order Processing iFlow
- Visualized BPMN diagram
- AI-generated summaries of each step
- Extracted Groovy logic with explanations

#### Example 2: iFlow with Custom Security and Error Handling
Result: 
A document that includes:

- Detailed security configurations
- Error handling logic
- AI-generated technical descriptions of mappings and endpoints

## 🧑‍💻 Code Explanation (Dynamic_generate_iflow_spec_using_ai.py)

### 1. Configuration Loading: 
Reads API keys, file paths, and settings from config_file.json.
### 2. Gemini API Integration: 
Sends XML fragments and Groovy scripts to Gemini for summaries.
### 3. XML Parsing: 
Extracts sections like overview, design, message flow, sender/receiver, mappings, security, error handling, and metadata.
### 4. Document Generation: 
Uses python-docx to build a Word document with headings, tables, diagrams, and formatted text.
### 5. BPMN Diagram: 
Generates visual diagrams using matplotlib and networkx.
### 6. Groovy Script Extraction: 
Summarizes Groovy logic using Gemini and embeds code and explanations.
### 7. Section Summarization: 
Each technical section is summarized using Gemini AI.
### 8. Tables and Formatting: 
Key properties and configurations are presented in color-coded tables.
### 9. Appendix and Metadata: 
Lists additional technical artifacts and metadata.

## 📚 References
Here are some resources to help you understand and utilize the project effectively:

- [SAP Community Blog Post](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-cloud-integration-ci-cpi-iflow-technical-specification-document/ba-p/14212348)
- [Google Gemini API Documentation](https://ai.google.dev/gemini-api/docs)


## 🤝 Contributing
If you'd like to contribute to this project, please feel free to submit a pull request. For major changes, we recommend discussing them first by opening an issue
