# Data Visualization: From Neo4j to Tableau

## 🎯 Project Overview  
This project demonstrates an end-to-end workflow for graph data visualization: ingesting and modeling data in the graph database Neo4j, then exporting and visualizing it in Tableau. The content is based on the accompanying tutorial video which walks through data preparation, graph schema design, exporting graph data, and building interactive dashboards.

## 🚀 Why This Matters  
- Graph databases excel at representing relationships and networks which are difficult in tabular systems.  
- Visualizing graph data in Tableau provides business-friendly dashboards, enabling exploration of network structures, path analysis, community detection, and more.  
- This workflow bridges graph analytics with enterprise BI tools, unlocking richer insights for decision makers.

## 🧰 What’s Included  
- `data/` – Sample dataset(s) used for ingestion into Neo4j (e.g., nodes, relationships CSV files).  
- `neo4j/` – Cypher scripts for schema creation, data import, and sample queries (e.g., finding shortest paths, computing centrality).  
- `export/` – Processed output (e.g., graph exports or aggregated tables) ready for consumption by Tableau.  
- `tableau/` – Tableau workbook(s) (`.twb` or `.twbx`) including dashboards, worksheets, and calculated fields built from the exported graph data.  
- `docs/` – Additional documentation: dataset description, schema diagram, dashboard screenshots, and tutorial notes.  
- `README.md` – This file, outlining the project, usage instructions, and next steps.

## 🔍 Key Workflow Steps  
1. Data Preparation in Neo4j  
   - Define node labels (e.g., `Person`, `Company`, `Transaction`) and relationship types (e.g., `INVESTS_IN`, `CONNECTED_TO`).  
   - Load CSVs into Neo4j using Cypher `LOAD CSV`, create constraints/indexes, and set up the graph schema.  
   - Run sample graph analytics (e.g., centrality, community detection) to surface insights.

2. Exporting Graph Data for Tableau  
   - Decide on the export format: simplified node/relationship tables or aggregated results.  
   - Export via `CALL apoc.export.csv.*` or through Cypher `RETURN …` into CSV.  
   - Ensure column headers and data types are Tableau-friendly (dates, numeric, categorical).

3. Visualizing in Tableau 
   - Import the exported CSV files into Tableau.  
   - Build data sources and define relationships or joins as needed.  
   - Create dashboards: network overview, relationship explorer, path finder, metrics summary.  
   - Implement interactive filters, highlight actions, tooltips and dashboard navigation.  
   - Share results via Tableau Public or Tableau Server.
