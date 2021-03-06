# はじめてのHTML②
## ブロック要素
株式会社ギブリー IT研修  
新田章太



### この研修の対象
- 非エンジニア
- 簡単なプログラミングに触れてみたい人
- HTMLとSEOの関連を深く理解したい人


## この研修の最終的なゴール


簡単なWebページをつくれるようになろう


[Web名刺](mycard/mycard.html)



### 前回までのおさらい
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>title</title>
  </head>
  <body>
  </body>
</html>
```


## 今日学習すること
### HTMLのブロック要素を理解しよう
1. ブロック要素とインライン要素
2. h1~h6要素(見出しタグ)
3. `<div>`要素と`<p>`要素
4. `<ul>`要素と`<li>`要素
5. `<table>`要素
6. まとめ


### 今日のゴール


```
<!DOCTYPE html>
<html lang="ja">
    <head>
        <meta charset="UTF-8">
        <title>新田章太のプロフィール</title>
    </head>
    <body>
        <h1>新田章太</h1>
        <h2>基本プロフィール</h2>
        <div class="profile">
          <p>株式会社ギブリー取締役。エンジニアの市場価値を高めるために仕事をしています。
          CODEPREPというオンラインプログラミング学習サービスをつくっています。
          </p>
          <h2>基本情報</h2>
          <ul>
            <li>年齢：27歳</li>
            <li>性別：男性</li>
          </ul>
          <h2>趣味・特技</h2>
          <ol>
            <li>プログラミング</li>
            <li>子育て</li>
          </ol>
        </div>
    </body>
</html>
```


[完成サンプル](mycard/index.html)



## 1. ブロック要素とインライン要素


要素は **ブロック要素** と **インライン要素** に大別されます。


### 1-1. ブロック(レベル)要素


`<div>` `<p>` などのブロック要素は、<br>
ほとんどのブラウザでブロック要素の前後に改行が入ります。


#### 代表的なブロック要素
```
<address>、<blockquote>、<center>、
<div>、<dl>、<fieldset>、
<form>、<h1>-<h6>、<hr>、
<noframes>、<noscript>、
<ol>、<p>、<pre>、<table>、<ul>
```


### 1-2. インライン要素


`<span>` `<strong>` などのインライン要素は改行しないので、<br>
ブロック要素の中で使用します。


#### 代表的なインライン要素
```
<a>、<abbr>、<acronym>、<b>、<basefont>、
<bdo>、<big>、<br>、<cite>、<code>、<dfn>、
<em>、<font>、<i>、<img>、<input>、
<kbd>、<label>、<q>、<s>、<samp>、<select>、
<small>、<span>、<strike>、<strong>、<sub>、
<sup>、<textarea>、<tt>、<u>、<var>
```


#### 1-3. まとめ
|ブロック要素|インライン要素|
|---|---|
|前後に改行が入る|前後に改行が入らない|
|・div<br>・p(段落)<br>・h1~h6(見出し)|・span<br>・strong(強調)<br>・img(画像)|



## 2. h1~h6(見出し)タグ


```
<!DOCTYPE html>
<html lang="ja">
    <head>
        <meta charset="UTF-8">
        <title>新田章太のプロフィール</title>
    </head>
    <body>
        <h1>新田章太</h1>
        <h2>基本プロフィール</h2>
          株式会社ギブリー取締役。エンジニアの市場価値を高めるために仕事をしています。
          CODEPREPというオンラインプログラミング学習サービスをつくっています。
    </body>
</html>
```


### 2-1. 見出しタグとは


![](http://imgcc.naver.jp/kaze/mission/USER/20130730/17/1028547/24/250x250x4978ae64ee31d0cd0a9b8f35.jpg)  
見出しタグ（`<h1>`~`<h6>`タグ）は、文書に見出しをつけ、 文書構造をわかりやすく伝えるために使用するタグです。


ウェブブラウザで表示した際に見出しタグはテキストが大きくなり太字で表示され、閲覧者に見出しであることがわかりやすく表示されます。


```
<h1>テキスト</h1>
<h2>テキスト</h2>
<h3>テキスト</h3>
<h4>テキスト</h4>
<h5>テキスト</h5>
<h6>テキスト</h6>
```


### 具体的な例
[見出しなしver](mycard/htag.html)<br>
[見出しありver](mycard/htag2.html)


### 2-2. 見出しタグの効果


#### ①ユーザが読みやすい
見出しタグを適切に使うと、そのページ内の文章の構成がはっきりとなり、ユーザーは、ページの内容をストレスなく理解できるようになるのだ。さらに複数のサイズの見出しを使い分けると、より正確に、そのコンテンツの階層構造をユーザーに伝えることができるようになる。


#### ②検索エンジンにも読みやすい(SEO効果)
検索エンジンロボットに対しても同じように、**そのコンテンツの構造を正確に伝える効果がある。**
そのため、そのコンテンツの**インデックスがより適切に行われる**ようになる。


このように、サイトのコンテンツを作るのであれば、ユーザービリティの面から見ても、**SEOの面から見ても、見出しタグの使用は必要不可欠**と言える。


### 2-3. 見出しの注意


#### ①ページ構成と関係ない意図で使わないこと


時々、見た目を調整することだけを目的として、見出しタグを使用してしまう人がいる。しかし、見出しタグはテキストの見た目を調整するためのものではなく、あくまでもページ上の階層構造をユーザーや検索エンジンにとって分かりやすく示すために使うものだ。


#### ②見出し1`<h1>`は１ページに１つにすること


h1タグは、そのページでもっとも重要なテキストに対して使用するタグだ。例えば、サイトのトップページであればサイトタイトルが、記事ページであれば記事タイトルが、そのページでもっとも重要なテキストだ。そのためりh1タグは、タイトルに設定するのが自然だ。


#### TIPS: title = h1 がベター
※h1とtitleタグには同じテキストを設定しておこう。
タイトルタグは、SEOの観点から見ると、そのページの要素の中でも最重要と言えるものだ。そしてh1タグも同じように、そのページ内で最も重要なテキストを示すためのタグだ。従って、両者には同じテキストを設定しておくことが望ましい。


#### ③見出しタグの順番を守ること


見出しタグは`<h1>`から始まり`<h6>`まであるが、`<h1>`の次に来るのは`<h2>`、`<h2>`の後に来るのは`<h3>`というように順番を守らなければいけない。


当たり前だが機械にとっても、わかりやすい構造の文章を書くことが相手の理解を深めることに繋がります。



## 3. `<div>`タグと`<p>`タグ


```
<!DOCTYPE html>
<html lang="ja">
    <head>
        <meta charset="UTF-8">
        <title>新田章太のプロフィール</title>
    </head>
    <body>
        <h1>新田章太</h1>
        <h2>基本プロフィール</h2>
        <div class="profile">
          <p>株式会社ギブリー取締役。エンジニアの市場価値を高めるために仕事をしています。
          CODEPREPというオンラインプログラミング学習サービスをつくっています。
          </p>
        </div>
    </body>
</html>
```


### 3-1. `<p>`タグ とは


![](http://imgcc.naver.jp/kaze/mission/USER/20130730/17/1028547/25/250x250x59192c042c09c563a6d0d792.jpg)
#### p = pragraph(段落)
段落タグ「p」はブロックレベル要素です。pタグの中に入れていいのはインライン要素のみになります。


#### 【このタグに入れられるもの】
a、img、span、strong、em…など


#### `<p>`タグは文章を囲むべし
要するに、基本的には文章を一塊に区切るときには`<p>`タグを使います。
`<p>`タグで囲うことにより、クローラーに正しく文章の意味を伝えることが出来ます。


また、`<img>`タグによる画像も`<p>`タグで囲うのが適切なようです。
`<img>`タグはインライン要素なので`<img>`タグで囲んでも問題ないです。


`<p>`タグにブロック要素を挟むことは出来ないので気をつけましょう。


初心者で間違えやすいのは、pの中にdivを入れてしまったり、pを入れ子にしてしまったり、hを入れてしまったり。divやpやhなどのブロックレベル要素をpの中に入れてはいけません。


### 3-2. `<div>`タグ とは


![](http://imgcc.naver.jp/kaze/mission/USER/20130730/17/1028547/23/250x250x495ba0e7dc7990dbbc8c5710.jpg)
#### div = division(区分)
構造タグ「div」はブロックレベル要素です。divタグの中には何でも入れることが出来ちゃいます。
divの中にdivなどブロックレベル要素を入れ子にしても問題ありません。


#### <div>タグは他に適切なタグがないときに使うべし
`<div>`タグには`<p>`タグのような意味合いは全くありません。
文章を`<div>`タグで囲んでも段落としてクローラーには伝わらないのです。


ただ単に「ひとかたまりの範囲として定義する」だけ、と覚えましょう。


`<div>`タグは`<p>`タグと違い入れ子もできるので凡庸ですが、
他に適切なタグがあるならばそちらを優先して使うべきです。


適切なタグが見当たらないからしょうがなく`<div>`タグを使う。
`<div>タ`グ使用の優先順位は最下位に位置づけましょう。


具体的な利用用途としては、ひとかたまりの範囲を **CSSでスタイリングするため**　が多いです。


#### 【このタグに入れられるもの】
div、h1～h6、p、ul、dl、ol、li、span、img、strong、em…など


### 3-3. `<div>`と`<p>`の違いまとめ


||`<p>`|`<div>`|
|---|---|---|
|要素|ブロック要素|ブロック要素|
|用途|**ひとつの段落**であることを表す際に使用。|**ひとかたまりの範囲**として定義する際に使用。|
|クローラー|読む|読まない|



## 4. `<ul>`・`<ol>`タグと`<li>`タグ


```
<!DOCTYPE html>
<html lang="ja">
    <head>
        <meta charset="UTF-8">
        <title>新田章太のプロフィール</title>
    </head>
    <body>
        <h1>新田章太</h1>
        <h2>基本プロフィール</h2>
        <div class="profile">
          <p>株式会社ギブリー取締役。エンジニアの市場価値を高めるために仕事をしています。
          CODEPREPというオンラインプログラミング学習サービスをつくっています。
          </p>
          <h3>基本情報</h3>
          <ul>
            <li>年齢：27歳</li>
            <li>性別：男性</li>
          </ul>
          <h3>趣味・特技</h3>
          <ol>
            <li>プログラミング</li>
            <li>子育て</li>
          </ol>
        </div>
    </body>
</html>
```


### 4-1. `<ul>`タグと`<ol>`タグとは


![](http://imgcc.naver.jp/kaze/mission/USER/20130730/17/1028547/26/250x250xff6bdb1204dfe783a9213d20.jpg)  
リストタグ「ul」や「ol」はブロックレベル要素です。箇条書きを行う時に使うタグです。


#### ulタグ
##### ul = unordered list（順序がないリスト）
`<ul>`タグを使用すると、ほとんどのブラウザで`<li>` で定義した各リストの先頭に黒丸を付加します。
（CSSを使用すれば、黒丸以外に、白丸や四角形、画像等を指定することもできます。）


#### olタグ
##### ol = ordered list（順序のあるリスト）
`<ol>`タグを使用すると、ブラウザは各リストの先頭に数字と「.」（ピリオド）を付加し、`<li>`タグで定義された各項目の番号は自動的に増加して表示します。


### 4-2. `<li>`タグ
「LI」とは「list item」の略で、リストの項目を表示するために使用するタグです。


`<li>`タグは、`<ul>～</ul>`または`<ol>～</ol>`タグのリスト内の箇条書きの要素として利用します。



## 5. `<table>`要素

```
<!DOCTYPE html>
<html lang="ja">
    <head>
        <meta charset="UTF-8">
        <title>新田章太のプロフィール</title>
    </head>
    <body>
        <h1>新田章太</h1>
        <h2>基本プロフィール</h2>
        <div class="profile">
          <p>株式会社ギブリー取締役。エンジニアの市場価値を高めるために仕事をしています。
          CODEPREPというオンラインプログラミング学習サービスをつくっています。
          </p>
          <h3>基本情報</h3>
          <ul>
            <li>年齢：27歳</li>
            <li>性別：男性</li>
          </ul>
          <h3>趣味・特技</h3>
          <ol>
            <li>プログラミング</li>
            <li>子育て</li>
          </ol>
          <h3>学歴・経歴</h3>
          <table border="1">
            <tr>
              <th>年月日</th>
              <th>学歴・職歴</th>
            </tr>
            <tr>
              <td>2008年3月</td>
              <td>千葉県立船橋東高校 卒業</td>
            </tr>
            <tr align="center">
              <td>2008年4月</td>
              <td>筑波大学 入学</td>
            </tr>
            <tr>
              <td>2012年3月</td>
              <td>筑波大学 卒業</td>
  　         </tr>
          </table>
        </div>
    </body>
</html>

```


### 5-1. `<table>`要素とは


ブロック要素の一つで、その名の通り、「テーブル（表）」を作成するためのタグです。


![](http://udemy.benesse.co.jp/wp-content/uploads/table-large.png)


このような表は、table要素と、**th要素**、**tr要素**、**td要素**を組み合わせることによって作成できます。


### 5-1. th要素


##### th = table header（テーブルの見出し）
![](http://udemy.benesse.co.jp/wp-content/uploads/th.png)
th要素では、表の「見出し」を作成することができます。上記の表のイメージだと、「名前」と「背番号」がth要素です。


### 5-2. tr・td要素


#### tr要素
##### tr = table row（テーブルの行）
![](http://udemy.benesse.co.jp/wp-content/uploads/tr-large.png)
tr要素は、表の行を定義するための要素です。


#### td要素
##### td = table data
![](http://udemy.benesse.co.jp/wp-content/uploads/td-large.png)
td要素は、表のデータを入れるための要素です。


### 5-3. table要素に追加できる属性の紹介


#### border属性（枠線）
``<table border>`を指定することで、テーブルに枠線を表示させることができます。これはborder属性と呼ばれています。


もし仮に、border属性を指定しなければ、枠線が消えます。


#### align属性（整列）
align属性は、要素内容の配置方向を設定するための属性です。


tr要素を中央寄せ（center）にするには、tr要素に「align=”center”」というコードを記述します。


th要素はデフォルトで中央寄せ（center）になります。


## 6. まとめ


### ブロック要素とインライン要素
違いは改行されるかされないか


### 見出しタグ
見出しを表すもの。キレイに構造的に書くことで、読み手だけでなく、Google先生にも理解してもらえる。


### div・pタグ
ブロック要素を表すタグ。
構造のみを表現するのがdiv、文章の段落として意味を持たせるのがpタグ。


### リストタグ
順序があるリストがol、ないリストがul。
liはそれぞれの子要素。リストの項目を表す。
