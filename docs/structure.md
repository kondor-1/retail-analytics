retail-analytics-data-platform/
│
├── README.md
├── .gitignore
├── requirements.txt
│
├── docs/
│   ├── architecture.md
│   ├── data_dictionary.md
│   ├── business_questions.md
│   └── diagrams/
│       └── architecture.png
│
├── data/
│   ├── raw/
│   │   └── api/
│   │       ├── products/
│   │       ├── users/
│   │       └── carts/
│   │
│   ├── bronze/          # lightly processed, still close to source
│   ├── silver/          # cleaned & normalized
│   └── gold/            # analytics-ready tables
│
├── src/
│   ├── ingestion/
│   │   ├── fetch_products.py
│   │   ├── fetch_users.py
│   │   ├── fetch_carts.py
│   │   └── __init__.py
│   │
│   ├── quality/
│   │   ├── validate_raw_data.py
│   │   └── expectations.py
│   │
│   ├── transformations/
│   │   ├── bronze_to_silver.py
│   │   ├── silver_to_gold.py
│   │   └── __init__.py
│   │
│   ├── warehouse/
│   │   ├── schema.sql
│   │   ├── create_tables.sql
│   │   └── load_tables.py
│   │
│   ├── orchestration/
│   │   └── pipeline.py
│   │
│   └── utils/
│       ├── config.py
│       ├── logger.py
│       └── helpers.py
│
├── notebooks/
│   ├── 01_data_profiling.ipynb
│   ├── 02_eda.ipynb
│   └── 03_forecasting.ipynb
│
├── dashboards/
│   └── retail_dashboard.pbix   # or tableau / screenshots
│
└── tests/
    ├── test_ingestion.py
    ├── test_transformations.py
    └── test_quality.py
