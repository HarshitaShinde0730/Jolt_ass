# Jolt_Assignment 
Welcome to the JOLT Assignment Repository! This repository contains the assignments and solutions for working with Java Object Language Transform (JOLT) transformations. Here, you'll find examples, explanations, and resources to deepen your understanding of JOLT specifications, including working with advanced transformations, wildcards, and nested JSON structures.

# Table of Contents
1. Overview
2. Assignments
3. Setup
4. Folder Structure
5. Usage
6. Examples

# Overview
This repository was created as part of a project to learn and implement JOLT transformations. JOLT is a powerful tool for transforming JSON data using a declarative transformation language, especially useful in Apache NiFi and data transformation workflows.

# Assignments
Each assignment in this repository covers a specific aspect of JOLT, from basic transformations to complex, conditional transformations with wildcards and nested data handling. Assignments include:

***1. Basic transformations: Mapping and filtering data.
2. Nested JSON transformations: Handling deeply nested structures.
3. Conditional transformations: Applying transformations based on specific field values.
4. Wildcard usage: Using #, $, and other symbols to manage dynamic key names and arrays.***

# Setup
To run the transformations:
[Nifi_download](https://nifi.apache.org/download/) and to run [jolt spec](https://jolt-demo.appspot.com/#inception) for more guidance visit [Nifi Doc](https://nifi.apache.org/docs/nifi-docs/)   

# Folder Structure
assignments/ – Contains individual assignments, each in a separate folder with:
input.json – Input JSON data for transformation.
spec.json – JOLT specification used for the transformation.
output.json – Expected output after applying the transformation.
examples/ – Additional examples for practice.
resources/ – Contains any supplementary resources and links for learning.

# Examples
Here's a simple example for transforming JSON data:

**Input JSON:**
**json**
{
  "orderId": "12345",
  "orderDate": "2024-11-10",
  "customer": {
    "name": "John Doe",
    "contact": "john.doe@example.com"
  }
}

**Spec JSON:**
[
  {
    "operation": "shift",
    "spec": {
      "orderId": "order.id",
      "orderDate": "order.date",
      "customer": {
        "name": "order.customerName",
        "contact": "order.customerContact"
      }
    }
  }
]

**Output JSON:**
**json**
{
  "order": {
    "id": "12345",
    "date": "2024-11-10",
    "customerName": "John Doe",
    "customerContact": "john.doe@example.com"
  }
}





