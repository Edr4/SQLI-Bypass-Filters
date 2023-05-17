# SQLI-Bypass-Filters

# MYSQL

## Databases 

### Count number of databases
```sql
SELECT count(DISTINCT(table_schema)) FROM information_schema.tables; 
```
### Get database name
```sql
SELECT DISTINCT table_schema FROM information_schema.tables LIMIT 1,1; # LIMIT 1 to result of count -1
```

## Tables

### Count number of tables
```sql
SELECT COUNT(TABLE_NAME) FROM information_schema.tables WHERE TABLE_SCHEMA = "table_name"; 
```

### Get table name
```sql
SELECT TABLE_NAME FROM information_schema.tables WHERE TABLE_SCHEMA = "table_name" LIMIT 0,1; # LIMIT 0 to result of count
```

## Columns

### Count number of columns
```sql
SELECT COUNT(COLUMN_NAME) FROM information_schema.columns WHERE TABLE_SCHEMA = "database_name" AND TABLE_NAME = "table_name"; 
```

### Get columns name
```sql
SELECT COUNT(COLUMN_NAME) FROM information_schema.columns WHERE TABLE_SCHEMA = "database_name" AND TABLE_NAME = "table_name" LIMIT 0,1; # LIMIT 0 to result of count
```
