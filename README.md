# UBC-MDS-Programming-Self-Test
import pandas as pd

# Read the data from the file
df = pd.read_csv("your_file_path.csv", delimiter='\t')

# Compute the mean and variance for each numeric column
result = df.groupby('country').agg({'lifeExp': ['mean', 'var'],
                                     'pop': ['mean', 'var'],
                                     'gdpPercap': ['mean', 'var']})

# Print the result
print(result)
