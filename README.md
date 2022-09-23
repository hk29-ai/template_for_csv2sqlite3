# csv2sqlite3_db  
csvファイルでなくて、sqlite3のデータベース（DB）を活用するPythonの雛形コードを載せました。  
  
コマンドラインでcsvからsqlite3のDBへ変換は、次のようにして行えます  
sqlite3 -separator , iris.db ".import iris-dataset.csv table_name"  
  
しかし、上記の方法で作成したDBのテーブルの型は、全てTEXT（文字列）になります。  
これでは数値データとして処理したい場合に不都合な場合があり得えます。例えば、ある数値データ列に対して、数値5以上7未満の値を有するデータ行を抽出したい場合等です。  
そのため、最初にDBを作成する際は、テーブルは手動で指定して、大量のデータ挿入はPythonの標準ライブラリsqlite3を用いると便利です。  
ちなみに、一度作成したDBへのデータの追加は挿入と同じです。  
  
  
## ■csv2sqlite3_db.ipynb  
Pythonを用いて、csvファイルをsqlite3のDBファイルを作成するJupyterLab用のファイルです。  
https://github.com/hkosa134/csv2sqlite3_db/blob/main/csv2sqlite3_db.ipynb  
  
## ■load_sqlite3_db_and_extract_data.ipynb  
sqlite3のDBを読み出して、条件を指定してデータを抽出する雛形コードをいくつか載せています。最後に、それをcsvファイルへ出力するコードも載せました。  
https://github.com/hkosa134/csv2sqlite3_db/blob/main/load_sqlite3_db_and_extract_data.ipynb  

