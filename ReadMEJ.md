ActiveReportsがSQLiteのデータソースのDateTimeを使う
---------------------------------------

DateTime型が使いたい。

DateTime型はSQLiteでは使えないと思っていた。

でもSQLiteのサンプルデータベースの中にDateTimeを見つけた。

ActiveReportsの日付の書式設置がSQLiteのDataTime Columnに使えるのでは？

SQLiteでDataTime型のカラムのあるテーブルを作ってみた。

そして試した。

動いた！！

.NetがSQLiteのDateTime型のカラムを本当のDateTime型に変換しているのかもしれない。

## 環境

- Windwows10 Pro x64
- [ActiveReports .Net Desinger 12J](https://www.grapecity.co.jp/developer/activereports)
- [SQLite3 ODBC Driver 32bit](http://www.ch-werner.de/sqliteodbc/sqliteodbc.exe)

ActiveReports .Net Designer と SQLite3 ODBC Driver 32bit版をインストールする必要があります。

### ファイル

- userlist
    - SQLiteで作ったDatabase
- sqlitedatetime.rdlx
    - ActiveReportsのreportsファイル
    - DataSource
        - DataProvider : ODBC 
        - ConnectionStrings: DRIVER={SQLite3 ODBC Driver};Database=userlist;
    - DataSet
        - Query : "select * from Users"
- ReadMe.md
    - 英語版のReadMe
- ReadMeJ.md
    - このファイル。

userlistの中のデータを見たい？

[DBeaver](https://dbeaver.io/)か[DB Browser for SQLite](https://sqlitebrowser.org/)をお勧めするよ。


### 実行方法

1. このフォルダの中のsqlitedatetime.rdlxを開く
2. プレビュー表示
3. 年号スタイルの日付と西洋スタイルの日付が表示されます。