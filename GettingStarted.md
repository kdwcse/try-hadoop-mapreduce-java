MacとWindowsで分けて記述しています。MacであればJDKとEclipseをインストール済みであれば、ソースをチェックアウトするだけで環境構築が出来ます。Windowsの場合は追加でCygwinのインストールが必要になります。なお、気軽に試すことを重視しているため、Mavenは利用していません。




---


# Macの場合 #

## ソースのチェックアウト(Mac) ##

http://try-hadoop-mapreduce-java.googlecode.com/svn/trunk/ から
「try-mapreduce」Eclipseプロジェクトをチェックアウトしてください。

## 動作確認(Mac) ##

「try-mapreduce」Javaプロジェクトの「src/main/java」ソールフォルダ内にある、「jp.gr.java\_conf.n3104.try\_mapreduce.WordCount」クラスをJavaアプリケーションとして実行して下さい。実行中に例外が発生せずにプログラムが終了したことを確認し、「target/output/WordCount」フォルダ内に「part-r-00000」というファイルが出力されていれば動作確認完了になります。


---


# Windowsの場合 #

## Cygwinのインストール ##

Hadoopは内部でLinuxコマンドを実行するためCygwinをインストールして下さい。2011-04-29時点の最新のsetup.exeでインストールを行い、動作することを確認しています。
http://cygwin.com/setup.exe

#### インストールパッケージ ####

デフォルトのままで問題ありません。スタンドアロンモードで利用するコマンドは分かっている範囲で以下の3つです。
  * bash
  * chmod
  * df

#### 環境変数PATHの追加 ####

Cygwinのコマンドがインストールされたディレクトリを環境変数PATHに追加して下さい。私の場合は「C:\cygwin\bin」を環境変数PATHの最後尾に追加して動作することを確認しています。

## ソースのチェックアウト(Win) ##

[ソースのチェックアウト(Mac)](http://code.google.com/p/try-hadoop-mapreduce-java/wiki/GettingStarted#ソースのチェックアウト(Mac))を参照して下さい。

## 動作確認(Win) ##

[動作確認(Mac)](http://code.google.com/p/try-hadoop-mapreduce-java/wiki/GettingStarted#動作確認(Mac))を参照して下さい。