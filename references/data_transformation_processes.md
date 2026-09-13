## Tools used:

1. **Python libraries**: Python is a flexible programming language commonly used for data analysis. Libraries add tools for cleaning, transforming, analyzing, and visualizing data.

  -    **Polars**: Polars is a fast DataFrame library designed for efficient data processing and analysis. It is especially useful for working with large datasets while using less memory and taking advantage of parallel processing.
  -    **Pandas**: Pandas is a Python library for organizing, cleaning, and analyzing tabular data. It provides flexible tools for filtering, grouping, reshaping, and summarizing datasets.
  -    **Marimo**: Marimo is a reactive Python notebook environment for interactive data analysis and development. It automatically updates dependent cells when code or data changes, helping keep notebooks consistent and reproducible.

2. **Database tools**: Microsoft SQL Server is a relational database system used to store, manage, and query structured data. It uses SQL to retrieve, update, and organize information across related tables. It also includes tools for security, reporting, automation, and large-scale data processing.
3. **Power BI's Power Query**: Power Query is a data preparation tool used to connect, clean, and transform data from many sources. It records transformation steps so the process can be repeated automatically when data is refreshed. Power Query is commonly used in Excel and Power BI to prepare data for analysis and reporting.

## Wide to Long:

Wide data places repeated values across many columns, which often resembles the format people are used to seeing in reports and spreadsheets. Long data stores those repeated values in rows, with separate columns identifying what each value represents. While wide data can be easier for people to read, long data is usually easier for software to filter, group, summarize, and visualize. Converting wide data to long format also makes it easier to add new periods, categories, or measures without continually creating new columns. For data analysis and database work, long data is generally more flexible and easier to maintain.

## How tools used transformed data wide to long:

### Power BI tools

Power Query was used to transform FDOE calculation data extracted from PDFs because the documents do not follow a consistent repeating structure. Tables, headings, page layouts, and column arrangements can vary across calculation periods and fiscal years, making fully automated extraction difficult.

Power Query was well suited for this work because its graphical interface made it easier to inspect each extraction and adjust the transformation process when document structures changed. The interface was used to:

* Remove unnecessary headers and rows.
* Rename and standardize columns.
* Fill values where needed.
* Filter irrelevant records.
* Reshape wide report tables into long format.
* Review and modify transformation steps when FDOE layouts changed.

### Python tools

Python was used for Excel, CSV, and text-based datasets because these formats generally have more predictable structures and can be processed efficiently with reusable code. Pandas or Polars was selected as appropriate for each dataset.

Python transformations included:

* Reading multiple source files.
* Standardizing column names and data types.
* Removing unnecessary rows and columns.
* Reshaping wide datasets into long format.
* Adding consistent identifying fields such as fiscal year, calculation period, and source information.
* Preparing standardized datasets for database loading and analysis.

Using Power Query for irregular PDF data and Python for more structured file formats provided a practical way to standardize FDOE data from many different sources. The resulting long-format datasets are easier to combine, query, analyze, and maintain over time.
