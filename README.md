Experiment-13
AIM: To study data cleaning techniques in Pandas including handling missing values, replacing data, type conversion, and formatting inconsistent data.
THEORY : pd.DataFrame(): Creates a DataFrame (tabular dataset) from structured data like dictionaries.

np.nan: Represents missing or undefined values in the dataset.

display(): Displays the DataFrame in tabular format (used in Jupyter/Colab).

df.isna(): Returns True for missing values and False for non-missing values.

df.notna(): Returns True for non-missing values and False for missing values.

df.isna().sum(): Counts missing values column-wise.

df.isna().sum(axis=1): Counts missing values row-wise.

axis parameter: axis=0 means column-wise operation, axis=1 means row-wise operation.

df.dropna(): Removes rows that contain missing values.

df.dropna(axis=1): Removes columns that contain missing values.

df.fillna(value): Replaces missing values with a specified constant value.

df.fillna(0): Replaces missing values with zero (may reduce accuracy).

df.mean(): Calculates the mean of numeric columns.

df.fillna(df.mean()): Replaces missing values using column-wise mean (best common practice).

df.apply(): Applies a function across rows or columns.

lambda function: A short anonymous function used inside apply().

Row-wise mean filling: df.apply(lambda row: row.fillna(row.mean()), axis=1) fills missing values using the mean of that specific row, not the column (used when row-wise relationships matter).

df.replace(): Replaces specific values (e.g., "-" with NaN).

inplace=True: Updates the existing DataFrame instead of creating a new one.

pd.to_numeric(): Converts column data to numeric type.

errors="coerce": Converts invalid values into NaN during conversion.

df.fillna(df.median()): Replaces missing values with median (useful for skewed data).

df["col"].str.upper(): Converts text data to uppercase for consistency.

pd.to_datetime(): Converts data into datetime format.

format="mixed": Allows multiple date formats in the same column.

dayfirst=True: Interprets dates in day/month/year format.

NaT (Not a Time): Represents invalid or missing datetime values.
CONCLUSION : In this experiment, we learned how to clean datasets by handling missing values using different techniques like dropna() and fillna(). We understood the difference between column-wise mean filling and row-wise mean filling. Data inconsistencies were corrected using replace(), type conversion, and formatting methods. Data cleaning improves the quality and reliability of analysis results.
