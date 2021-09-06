# Birthdates

シングル HTML ファイル・ローカルでも動作する誕生日管理アプリ。


## Demo

__[Enter The Demo Site](https://neos21.github.io/birthdates/)__

- [Demo Data (URL Parameters)](https://neos21.github.io/birthdates/?c0=ExampleA,1991-01-01,ExampleB,1992-02-02&c1=ExampleC,1993-03-03,ExampleD,1994-04-04)


## How To Use

人名と誕生日情報を、HTML 中にベタ書きするか、URL パラメータで指定できる。

### HTML 中にベタ書きする

`index.html` を開き、`body` 要素内・`#title` 要素の後ろに、次の要領で情報を記述していく。

- 改行を入れたい場合は `.container` で区切る
- 一人分の情報を `.person` でまとめ、配下に `.name` と `.birthdate` を記述する
- `.birthdate` 内は `YYYY-MM-DD` 形式での指定を推奨する

```html
<div class="container">
  <div class="person">
    <div class="name">ExampleA</div>
    <div class="birthdate">1991-01-01</div>
  </div>
  <div class="person">
    <div class="name">ExampleB</div>
    <div class="birthdate">1992-02-02</div>
  </div>
</div>
<div class="container">
  <div class="person">
    <div class="name">ExampleC</div>
    <div class="birthdate">1993-03-03</div>
  </div>
  <div class="person">
    <div class="name">ExampleD</div>
    <div class="birthdate">1994-04-04</div>
  </div>
</div>
```

### URL パラメータで指定する

上述の HTML 相当の情報を、URL パラメータ (クエリ文字列) で指定する場合は次のように記述する。

- `c0`・`c1` といった単位で `.container` 要素を作れる。連番を必ず付与する
- 各パラメータは `名前,YYYY-MM-DD` をカンマ区切りで記述していく
- `position=end` パラメータを付与すると、`body` の終了タグ直前に挿入する (= HTML 中にベタ書きした情報の後ろに挿入される)。デフォルトでは `#title` 要素の直後に挿入される

```
/PATH/TO/birthdates/index.html?c0=ExampleA,1991-01-01,ExampleB,1992-02-02&c1=ExampleC,1993-03-03,ExampleD,1994-04-04
```


## Customize

CSS・JavaScript ともに `index.html` 内にベタ書きしている。外部リソースを一切利用しないので、`index.html` 内の記述を変更することでデザインや処理を独自にカスタマイズできる。


## Links

- [Neo's World](https://neos21.net/)
- [GitHub Pages - birthdates : Birthdates](https://neos21.github.io/birthdates)
