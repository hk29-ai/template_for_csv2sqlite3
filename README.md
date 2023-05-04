# 概要  
sqlite3のデータベース（DB）を読み込んで、データを抽出したり、csvファイルへ出力するPythonの雛形コードを載せました。   
  
## ■csv2sqlite3_db.ipynb  
Pythonを用いて、csvファイルをsqlite3のDBファイルを作成するJupyterLab用のファイルです。  
https://github.com/hk29-ai/csv2sqlite3_db/blob/main/template_for_csv2sqlite3db.ipynb  
  
## ■load_sqlite3_db_and_extract_data.ipynb  
sqlite3のDBを読み出して、条件を指定してデータを抽出する雛形コードをいくつか載せています。最後に、それをcsvファイルへ出力するコードも載せました。  
https://github.com/hk29-ai/csv2sqlite3_db/blob/main/template_for_load_sqlite3db_and_extract_data.ipynb  

## 備考  
コマンドラインでcsvからsqlite3のDBへ変換は、次のようにして行えます  
sqlite3 -separator , iris.db ".import iris-dataset.csv table_name"  
  
しかし、上記の方法で作成したDBのテーブルの型は、全てTEXT（文字列）になります。この場合、ある指定した数値区間、例えば5以上7未満の値を有するデータ行を抽出したくともできません。  
そのため、最初にDBを作成する際は、テーブルは手動で指定して、大量のデータ挿入はPythonの標準ライブラリsqlite3を用いると便利です。一度作成したDBへのデータの追加は挿入と同じです。  
