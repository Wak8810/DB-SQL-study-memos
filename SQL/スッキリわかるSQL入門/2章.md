改行、空白はOK
セミコロンで終了
ハイフン二つ、/\*\*/でコメント
予約語は小文字も可能

データそのものの値はリテラルと呼ぶ

型の種類
小数
DECIMAL,NUMERIC,FLOAT,DOUBLE,REAL
文字列
固定長CHAR
可変長VARCHAR
日付
TIMESTAMP,DATETIME,DATE,TIME

## 命令体型4種
DML(Data Manipulation Language)と呼ばれる

| 命令     | 命令固有の部分                                     | 対象行の絞り込み | 検索結果の加工 |
| ------ | ------------------------------------------- | -------- | ------- |
| SELECT | 列名...FROM table                             | WHERE    | その他修飾   |
| UPDATE | table SET column = value ...                | WHERE    |         |
| DELETE | FROM table                                  | WHERE    |         |
| INSERT | INTO table (column...)<br>VALUES (value...) |          |         |

- 学ぶ上で大事なこと
	- 構造と就職後の全体像を把握
	- 2通りの分類方法を理解
		- 検索と更新
			- SELECT
			- UPDATE DELETE INSERT
		- 既存と新規
			- SELECT UPDATE DELETE
			- INSERT
	- テーブル指定を先に書く
		- 固有部分のみについて以下
		- 順番として、
			- 命令
			- テーブル指定
			- その後ろ
			- SELECTは列名
		- と書くと良い

| 命令     | 1     | テーブルの指定    | その他                   |
| ------ | ----- | ---------- | --------------------- |
| SELECT | 列名... | FROM table |                       |
| UPDATE |       | table      | SET 列名=値...           |
| DELETE |       | FROM table |                       |
| INSERT |       | INTO table | (列名...) VALUES (値...) |

## SELECT
- column,table後にASを付けると、その名前で出力される
	- column as name, column as name,...
	- Oracleはtable後のASなし
## UPDATE,DELETE
- 大体WHERE使うべ
- INSERTと違って、更新する時は、SET カラム=値
## INSERT
- カッコ必要なの忘れがち
	- テーブル以外(カラムとフィールド)は囲う
