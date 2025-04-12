# Microsoft Dataflow to Databricks Pipeline Migration

This comprehensive notebook automates the migration of Microsoft Dataflows into a Databricks pipeline. It retrieves the full dataflow definition from the source API, translates each transformation step from the M language (Power Query) into equivalent PySpark code, and then automatically generates a new Databricks notebook that implements the complete pipeline.

## Key Features

- **Full Dataflow Extraction**: Retrieves all transformation steps (extract, filter, join, aggregate, pivot, etc.)
- **Comprehensive Translator**: Converts a wide array of common Dataflow functions to PySpark:
  - **Extract & Load**: Reading source files in various formats
  - **Filtering & Conditional Logic**
  - **Renaming & Type Conversion**
  - **Joins, Merge, and Append**
  - **Aggregation, Grouping and Sorting**
  - **Pivot and Unpivot operations**
  - **Date/Time transformations**
  - **Text Manipulations and Replacements**
  - **Column Splitting and Custom Scripts**
- **Delta Lake Integration**: Optionally materializes intermediate results as Delta tables
- **Automated Notebook Generation**: Builds a complete pipeline notebook with detailed markdown documentation for each step

## Prerequisites

1. **Databricks Environment** with PySpark configured
2. **API Access** to your Microsoft Dataflow definitions
3. **Python Dependencies**: `msal`, `requests`, `nbformat`
