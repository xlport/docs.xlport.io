# Excel to JSON

## importFromFile

Reads data from Excel tables or individual cells

### arguments

`file`: data file in XLSX or XLSM format 

`request`: contains "instructions" on what to extract.

### request

`properties`: List of cell names whose values are to be extracted.

`tables`: Object with Excel template table names as keys, and list of column names to be extracted as values.

