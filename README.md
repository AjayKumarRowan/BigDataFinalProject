# Data Visualization: From Neo4j to Tableau  

## 📌 Project Overview  
This project demonstrates an end-to-end workflow for graph data visualization: ingesting and modelling data in Neo4j, then exporting and visualizing it in Tableau. It follows the tutorial shown in the accompanying video.  
Link to video: [Data Visualization: From Neo4j to Tableau](https://youtu.be/nZbu3swXn30)  

## 🎯 Why This Matters  
- Graph databases excel at representing relationships and networks that are difficult to model in traditional tabular systems.  
- Visualizing graph-data in Tableau enables business stakeholders to explore network structures, path analysis, centrality, communities, etc.  
- This workflow bridges graph analytics (Neo4j) with enterprise BI tools (Tableau) thereby unlocking richer insights for decision-makers.

## 🧩 What’s Included  
- `IPL_Ball_by_Ball_2008_2022.csv` & `IPL_Matches_2008_2022.csv` – raw CSV datasets of Indian Premier League (IPL) matches and ball-by-ball events.  
- `Neo4j.txt` – Cypher key commands / script snippets for schema creation and data import into Neo4j.  
- `BigDataFinalproject.twb` (and/or `.twbx`) – Tableau workbook file(s) containing dashboards built from graph exports.  
- `logo/` – branding or presentation logos (optional).  
- `steps.png` – a graphic or flowchart documenting the workflow steps or the project pipeline.  
- `README.md` – this file, explaining the project, usage instructions, and next steps.

## 📝 Key Workflow Steps  
1. **Data Preparation in Neo4j**  
   - Define node labels (for example: `Player`, `Team`, `Match`), and relationship types (`PLAYED_FOR`, `COMPETED_IN`, `WICKET_TAKEN`, etc).  
   - Load CSVs into Neo4j using `LOAD CSV`, create constraints and indexes, set up the graph schema.  
   - Perform sample graph analytics: shortest paths, player-centrality, community detection among teams.  
2. **Exporting Graph Data for Tableau**  
   - Decide on export format: Node table and Relationship table or aggregated result tables.  
   - Export using `CALL apoc.export.csv.*` procedures or via `RETURN …` statements into CSV files compatible with Tableau.  
   - Ensure column headers and data types align with Tableau’s requirements (e.g., dates, numeric, categorical).  
3. **Visualizing in Tableau**  
   - Import the exported CSV files into Tableau and set up data sources/joins as needed.  
   - Build interactive dashboards: e.g., network overview of players-teams, highlight filters for top wicket-takers, timeline of matches, etc.  
   - Implement Tableau features: filters, highlight actions, tooltips, dashboard navigation.  
   - Publish the workbook (if desired) via Tableau Public or Tableau Server for sharing.
