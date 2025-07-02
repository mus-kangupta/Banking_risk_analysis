query ="select * from banking_case.customer"
import pyodbc
import pandas as pd

# Set connection
conn = pyodbc.connect(
    'DRIVER={SQL Server};'
    'SERVER=DESKTOP-G7S52L1;'
    'DATABASE=banking_case;'
    'Trusted_Connection=yes;'
)

# Fetch the full table into a DataFrame
df = pd.read_sql("SELECT * FROM customer", conn)
print(df)

# Display the first 5 rows
df.head()
