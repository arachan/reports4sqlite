ActiveReports use DateTime in SQLite Datasource.
---------------------------------------

I want to use DateTime type.

I think SQLite don't use DateTime.

But,I found DateTime in Sample Database on SQLite.

Do ActiveReports use Date Formatting DateTime Column on SQLite DataSource ?

I make table in DateTime Type Columns on SQLite.

I have tried.

Success !!

.Net may convert true DateTime to read DateTime Type coloumns on SQLite.

## Emvironment

- Windwows10 Pro x64
- [ActiveReports .Net Desinger 12J](https://www.grapecity.co.jp/developer/activereports)
- [SQLite3 ODBC Driver 32bit](http://www.ch-werner.de/sqliteodbc/sqliteodbc.exe)

You need to install ActiveReports .Net Designer and SQLite3 OCBC Driver for 32bit.

## Files

- userlist
    - SQLite Database
    - Users Table in this database.
- [sqlitedatetime.rdlx](sqlitedatetime.rdlx)
    - ActiveReports reports file
    - DataSource
        - DataProvider : ODBC 
        - ConnectionStrings: DRIVER={SQLite3 ODBC Driver};Database=userlist;
    - DataSet
        - Query : "select * from Users"
- ReadMe.md
    - This File
- [ReadMEJ.md](ReadMEJ.md)
    - Japanese ReadMe.


Do you want to show data on userlist?

I recommend to use [DBeaver](https://dbeaver.io/) or [DB Browser for SQLite](https://sqlitebrowser.org/).

## How to Execute

1. Open sqlitedattime.rdlx in This folder.
2. Preview.
3. show Name and Japanese Imperial era and Western Style date.