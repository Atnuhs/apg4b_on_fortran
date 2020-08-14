
# No.2 エラーを直してみる

## 問題文

Kくんは次の出力をするプログラムを作ろうとしました｡

### 実行結果

``` text
ギャバを食べて､体がギャバギャバしてきた｡
「エナンチオマー」
```

しかし､書いたプログラムを実行してみるとエラーが発生しました｡
Kくんが書いたプログラムのエラーを修正し､正しく動作するようにしてください｡

#### Kくんが書いたプログラム

``` fortran
program main
    impricit none

    print(ギャバを食べて､体がギャバギャバしてきた｡)
    print(「エナンチオマー」)
program end
```

このコードを実行すると､標準エラー出力に以下のエラーメッセージが表示されます｡

``` text
test.f90:2:4:

     impricit none
    1
Error: Unclassifiable statement at (1)
test.f90:4:9:

     print(ギャバを食べて､体がギャバギャバしてきた｡)
         1
Error: Syntax error in PRINT statement at (1)
test.f90:5:9:

     print(「エナンチオマー」)
         1
Error: Syntax error in PRINT statement at (1)
test.f90:6:11:

 program end
           1
Error: Unexpected PROGRAM statement at (1)
f951: Error: Unexpected end of file in ‘test.f90’
```

#### この問題の取り組み方

Kくんのプログラムには複数のエラーが含まれています｡
わかるエラーから一つずつ直し､コンパイルしてみて､治っているかどうか確かめましょう｡