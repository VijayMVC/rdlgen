# SSRS RDL Builder

A Python utility to generate an SSRS-compatible [RDL](https://msdn.microsoft.com/en-us/library/ms155062.aspx) file based on a simple SQL query.

## Usage

    python rdlgen.py [server_url] [datasource] < sqlfile.sql
    
Example:

    python rdlgen.py https://example.com/ReportsWebService "Reports" < report.sql

The SQL file is read from stdin, and a report containing all of the fields from the query in a simple table is created.

The output RDL file is stored as `output.rdl` in the current path by default.