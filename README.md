# CP/M 2.2 player for generic MS-DOS

汎用MS-DOS環境下で CP/M用に書かれた  
8080CPU用ソフトウエアを実行するプログラムです。  

## ビルド環境

OS：MS-DOS  
アセンブラ：Microsoft Macro assembler 6.00AD  

ファイル構成  
80.ASM --- ソースファイル  
80.LST --- MASMが生成するリスティングファイル  
80.OBJ --- MASMが生成するオブジェクトファイル  
80.COM --- MASMが生成する実行ファイル  

コマンドラインにて ml [/Fl] 80.asm
により直接80.COMが生成されます。

## 使い方

MS-DOS環境にて、カレントディレクトリ  
または環境変数Z_EMが示すディレクトリに  
8080エミュレータである8080EM.BINおよび8080用ソフトを置き  

80 8080ソフト名 8080ソフトに渡すパラメータ  
として実行ください。  
本プログラム自身のの実行時オプション（パラメータ）はありません。  

本ソフトでは8080の命令をソフトウエアエミュレータで実行し  
CP/MのBDOSファンクションコールとBIOSコールを  
MS-DOSのファンクションコールに置き換え処理します。  

CP/Mのソフトからはカレントディレクトリにあるファイルしか扱えません。  

一部、CP/MのファイルシステムとMS-DOSのファイルシステムで  
互換性がないファクションは、その旨表示し、実行を中止します。  

## 8080エミュレータ

8080機械語を解釈実行する部分は別モジュールとして分離しています。  
詳細は下記リポジトリをご参照ください。  
https://github.com/Gazelle8087/8080-instruction-executor-for-x86

## ライセンス

MITライセンスとします。

## 変更履歴
2024/8/22 Rev. 1.00	初回公開


