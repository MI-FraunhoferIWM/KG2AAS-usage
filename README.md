# Knowledge Graph to AAS JSON Conversion Pipeline

This repository demonstrates how to transform an **OWL/RDF-based Knowledge Graph (KG)** into a valid  
**Asset Administration Shell (AAS) JSON** representation using a sequential, transparent workflow.

The goal is to provide an educational, easy-to-follow demonstration of how semantic knowledge can be
mapped to the AAS 3.0 metamodel using SPARQL, RDF tooling, and the `py-aas-rdf` library.

---

## 🚀 Overview

This project shows how to:

1. Retrieve a Knowledge Graph from a remote data service (e.g., DSMS)
2. Apply a **SPARQL CONSTRUCT** mapping to convert domain semantics → AAS semantics
3. Convert the mapped RDF into AAS objects using `py-aas-rdf`
4. Serialize the result into **AAS-compliant JSON**
5. Validate against the official **AAS JSON Schema**
6. Save final AAS JSON files for downstream use

The notebook uses a **fully sequential approach** (no abstractions, no functions) for maximum clarity.

---

## 📁 Repository Structure

```plaintext
KG2AAS-usage/
├── input/
│   ├── mapping.sparql # SPARQL CONSTRUCT file for semantic transformation
├── output/
│   └── ... # Generated AAS JSON files
├── KG2AAS_demo.ipynb # Main sequential demonstration notebook
├── .env_template # Environment variables required to access DSMS instance(HOST_URL, credentials, etc.)
├── requirements.txt # Python dependencies
└── README.md # Project documentation
```

## 🔧 Requirements

Install all dependencies via:

```bash
pip install -r requirements.txt

## ⚙️ Configuration

Environment variables must be defined in a .env file in the working directory:

````plaintxt
DSMS_HOST_URL=https://pmdx.materials-data.space/
DSMS_USERNAME=<username>
DSMS_PASSWORD=<password>
```
