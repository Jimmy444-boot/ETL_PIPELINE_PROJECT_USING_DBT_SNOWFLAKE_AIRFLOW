# ETL_PIPELINE_PROJECT_USING_DBT_SNOWFLAKE_AIRFLOW
# ❄️ ELT Pipeline with dbt, Snowflake & Airflow

This project demonstrates the implementation of a modern ELT (Extract, Load, Transform) pipeline using **dbt**, **Snowflake**, and **Apache Airflow**. It is designed to take raw data, transform it into analytics-ready datasets, and orchestrate the entire process in a reliable and scalable way.

---

## 🔧 Tools & Technologies

- **Snowflake** – Cloud-based data warehouse for storing and querying data.
- **dbt (data build tool)** – For building modular SQL models, data testing, and documentation.
- **Apache Airflow** – For scheduling and orchestrating ELT workflows.

---

## 🧱 Project Steps

### Step 1: Setup Snowflake Environment

The first step involves setting up the Snowflake environment, including:

- Creating the required **warehouse**, **database**, **schema**, and **roles**.
- Loading raw data into Snowflake tables, which serves as the foundation for transformations.

---

### Step 2: Configure `dbt_profile.yml`

Configured dbt to connect to the Snowflake account by editing the `profiles.yml` file with appropriate credentials and environment details. This allows dbt to run models and manage data within Snowflake.

---

### Step 3: Create Source and Staging Files

- Defined **source files** to reference raw tables.
- Built **staging models** to perform light transformations, such as renaming columns, filtering, and type conversions.
- Used staging models as the foundation for all downstream transformations.


### Step 4: Use Macros (D.R.Y. Principle)

- Developed custom **macros** to reuse SQL logic across multiple models.
- Ensured consistency and reduced duplication by applying the **Don't Repeat Yourself (D.R.Y.)** principle.
- Macros included reusable snippets for things like column selection and timestamp formatting.

---

### Step 5: Build Transform Models

- Created **core models** such as fact and dimension tables.
- Organized transformations into **data marts** aligned with business domains.
- Built modular and layered dbt models to improve clarity and maintainability.

---

### Step 6: Add Generic and Singular Tests

- Applied **generic tests** like `not_null`, `unique`, and `accepted_values` to enforce data quality.
- Created **singular tests** to validate specific business rules and assumptions.
- Ensured that every model was tested to prevent data quality issues.

---

### Step 7: Deploy on Airflow

- Developed an **Airflow DAG** to schedule and orchestrate dbt tasks.
- Automated the pipeline to run on a regular schedule (e.g., daily).
- Ensured that transformations and tests are executed consistently in production.

---

## ✅ Outcome

The final result is a robust ELT pipeline that delivers clean, validated, and analytics-ready data in Snowflake. dbt makes the transformation process transparent and testable, while Airflow ensures reliable scheduling and orchestration.

This setup provides a scalable foundation for data engineering and analytics teams to build upon.



