# clue

MySql:

Fill gaps between number rows:
```mysql
SELECT MIN(l.column_name + 1) as nextavabile
from table_name as l
         LEFT OUTER JOIN table_name as r on l.column_name + 1 = r.column_name
WHERE r.column_name is NULL
```
