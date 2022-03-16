## General instructions

- Create 9 groups of 2 students and 1 group of 3 students
- Do the work in [Databricks Community Edition](https://community.cloud.databricks.com)
- To validate the project, send the following to **petra@adaltas.com**:
  - **One** notebook per group. It needs to contain the code that served to answer the questions. It should be readable (titles, comments, you can write text if you want).
  - **One** report in pdf format
  - *Don't forget to list all the authors in the mail and the report!*

Deadline: TBA

## Questions

You need to answer the questions below. They are already present in the notebook `Lab2`. However, there are some extra questions in the notebook, that you don't need to do for the project.

- Read the us-counties.csv file and infer schema (dbfs:/databricks-datasets/COVID/covid-19-data/live/us-counties.csv)
- Check the schema. What type is the date column?
- Convert `date` from string to date type.
- First day in the dataset.
- Last day in the dataset.
- Aggregate confirmed cases and confirmed deaths per state (by `sum`).
- Which state has the max confirmed cases?
- Which state has the max confirmed deaths?
- Do we have the data for all the states?
- How many counties is in each state?
- Create dataframe `masks` by reading `dbfs:/databricks-datasets/COVID/covid-19-data/mask-use/mask-use-by-county.csv`.
- Create a new column with two groups of frequency of wearing masks: `almost_never` (NEVER+RARELY) and `almost_always` (FREQUENTLY+ALWAYS). Name the table `masks_groups`.
- Join the tables `masks_groups` and `counties`. Name the table `mask_use`.
- What happened during the join? Count lines for `counties`, `mask_groups` and `mask_use`.
- Keep data for only one state (whichever you want).
- How would you visualize the frequency groups? Make a plot.
- Save `mask_use` as a Parquet file.
