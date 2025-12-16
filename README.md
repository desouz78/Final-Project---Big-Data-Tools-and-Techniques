# Brazilian Rural Schools Network in Neo4j

This is a Final Project implementation for the **Big Data Tools and Techniques** course at Rowan University, Fall 2025, visualizing Brazilian rural schools and their internet connectivity using Neo4j.

## Project Overview

The goal of this project is to create a **graph database** to represent rural schools in Brazil and their internet connections:

- **States** and **Cities** are nodes.
- **Schools** are nodes connected to their respective cities.
- **Technologies** are nodes representing the type of internet connection used.
- Relationships capture how schools are connected to technologies and cities, including important properties:

| Property | Description |
|----------|-------------|
| DescSituacao | Installation status of the internet service |
| TipoObrigacao | Type of obligation (program/funding) |
| VelAcessoInstalada | Installed access speed |
| NomePrestadora | Service provider name |
| DataAtivacao | Activation date |

This structure allows for **graph-based analysis** of schools by state, city, technology, and provider.

## Dataset

- Original dataset obtained from the Brazilian National Telecommunications Agency (ANATEL).  
- File used: `Relacao_Escolas_Rurais_Atendidas.csv`  
- Total rows: 29,012  
- Columns: 11  
- Source: [ANATEL Open Data Portal](https://dados.gov.br/dados/conjuntos-dados/escolas-rurais-conectadas)

> Note: Due to download restrictions, the CSV was uploaded to a personal Cloud Drive for access.

## Project Structure

All project files are organized as follows:

```
brazilian-rural-schools-neo4j/
  Relacao_Escolas_Rurais_Atendidas.csv   # Main dataset
  upload_to_neo4j.py                     # Python script to upload CSV data to Neo4j
  notebooks/
    FinalProject.ipynb                    # Jupyter notebook with all steps
  README.md
```

## How to Run

1. Install required libraries:

```bash
pip install pandas neo4j gdown
```

2. Ensure the CSV file is available locally (or download via `gdown`).  

3. Update Neo4j Aura credentials in `upload_to_neo4j.py`:

```python
uri = "neo4j+s://<your-database>.databases.neo4j.io"
user = "<your-username>"
password = "<your-password>"
```

4. Run the Python script (Jupyter notebook) provided to upload all data to Neo4j.

## Visualizations

Once uploaded, you can explore:

- Graph structure in Neo4j Browser or Neo4j Bloom.  
- Number of schools per state or city.  
- Technologies and providers distribution.  

## License

This project is for **educational purposes** only.
