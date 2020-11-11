# csv-splitter

A simple Python script to split big csv files (or any text files) into smaller ones.

## Using this script

1. Install the requirements

     ```pip install requirements.txt```

2. **Optional** Inspect the top of the large file you want to split, to check how many header rows there are

    ```head -10 /path/to/big/csv/file.csv```

3. Run the script, setting the `header_size` and `chunk_size` if necessary (the defaults are one header row and chunks of one million lines)

    ```python csv-splitter.py <filename> [--header_size=<lines>] [--chunk_size=<lines>]```

For example, to split a file into chunks of (the default) one million rows with a three-line header:

```python csv-splitter.py "/path/to/big/csv/file.csv" --header_size=3```
