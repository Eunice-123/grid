# grid
Install libraries in R : SF,dplyr, maps,tidyverse, Rpostgres, DBI, RODBC,odbc

- Importing layers that were in EPSG 27700
- create a start time 
- Creating grid in 27700
- creating centroids in country grid (27700)
- Splitting centriod coordinate into x 27700 and y 27700
- Transforming centriods to 3857
- Splitting centriods into x 3857 and y 3857
- Merging result from split 27700 and 3857
- Transforming grid to 4326
- unlisting grid 4326 into 5 pairs of coordinates 
- Merging all splitted columns
- Intersecting merge columns with grid
- Calculating area of grids
- Filtering area less than grid square say 4meters
- Generating unique ids for results
- Renaming columns
- Generating dates and author for all row 
save a dataframe object of result from grid of results say "b"
  # Creating local connection to postgres db
  -create postgis extension in db
  - in postgres create a table with the required headers from grid

# Local connection parameters
- DB_NAME = "***"
- DB_HOST = "***"
- DB_PORT = "***"
- DB_USERNAME = "***"
- DB_PASSWORD = "***"
- using con <- dbConnect(odbc::odbc(),"***")
- st_write(obj = b, dsn = con, Id(schema="posgres db schema", table = "postgres table"), append = TRUE)
- loop a list of selected grids in the function
- apply list on function 
