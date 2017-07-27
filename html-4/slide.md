# はじめてのHTML④
## 高度なメタ要素
株式会社ギブリー IT研修  
新田章太


### この研修の対象
- 非エンジニア
- 簡単なプログラミングに触れてみたい人
- HTMLとSEOの関連を深く理解したい人


## この研修の最終的なゴール


簡単なWebページをつくれるようになろう


[Web名刺](mycard/mycard.html)


ちょっとWeb名刺から離れつつあるゴール。笑
すみません、CSSまでやれていません。



### 前回までのおさらい
```
<!DOCTYPE html>
<html lang="ja">
    <head>
        <meta charset="UTF-8">
        <title>新田章太のプロフィール</title>
    </head>
    <body>
        <h1>新田章太</h1>
        <a href="https://facebook.com/maximum80"><img src="./images/avatar.png" alt="新田章太のプロフィール画像" width="150" height="150"></a>
        <h2>基本プロフィール</h2>
        <div class="profile">
          <p><a href="https://givery.co.jp" target="_black" rel="nofollow">株式会社ギブリー</a>取締役。エンジニアの市場価値を高めるために仕事をしています。
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


## 今日学習すること
### HTMLの高度なメタ要素を理解しよう
1. OGPとは
2. OGPの種類と設定方法
2. Facebookの設定
3. Twitter Cardの設定


### 今日のゴール


```
<!DOCTYPE html>
<html lang="ja">
    <head>
        <meta charset="UTF-8">
        <!-- Open Graph Protocol の設定-->

        <meta property="og:title" content="新田章太のプロフィール" />
        <meta property="og:type" content="website" />
        <meta property="og:url" content="https://givery-technology.github.io/it-training/html-4/mycard/index.html" />
        <meta property="og:image" content="https://givery-technology.github.io/it-training/html-4/mycard/images/haru.jpg" />
        <meta property="og:site_name" content="新田章太のプロフィール" />
        <meta property="og:description" content="株式会社ギブリー取締役。エンジニアの市場価値を高めるために仕事をしています。CODEPREPというオンラインプログラミング学習サービスをつくっています。" />
        <!-- ここまで -->

        <!-- Facebookの設定 -->
        <meta property="fb:app_id" content="120388268586719" />
        <!-- Twitter Cardの設定-->
        <meta name="twitter:site" content="@maximum_80" />
        <meta name="twitter:card" content="summary" />

        <title>新田章太のプロフィール</title>
    </head>
    <body>
      <div id="fb-root"></div>
      <script>(function(d, s, id) {
        var js, fjs = d.getElementsByTagName(s)[0];
        if (d.getElementById(id)) return;
        js = d.createElement(s); js.id = id;
        js.src = "//connect.facebook.net/ja_JP/sdk.js#xfbml=1&version=v2.10&appId=812950015465567";
        fjs.parentNode.insertBefore(js, fjs);
      }(document, 'script', 'facebook-jssdk'));</script>

        <h1>新田章太</h1>
        <a href="https://facebook.com/maximum80"><img src="./images/avatar.png" alt="新田章太のプロフィール画像" width="150" height="150"></a>
        <h2>基本プロフィール</h2>
        <div class="profile">
          <p><a href="https://givery.co.jp" target="_black" rel="nofollow">株式会社ギブリー</a>取締役。エンジニアの市場価値を高めるために仕事をしています。
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
        <div class="fb-share-button" data-href="https://givery-technology.github.io/it-training/html-4/mycard/index.html" data-layout="button_count" data-size="small" data-mobile-iframe="true"><a class="fb-xfbml-parse-ignore" target="_blank" href="https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fgivery-technology.github.io%2Fit-training%2Fhtml-4%2Fmycard%2Findex.html&amp;src=sdkpreparse">シェア</a></div>
    </body>
</html>
```


[完成サンプル](mycard/index.html)



## 1. OGPとは


### OGP
OGP とは [Open Graph Protocol (オープン・グラフ・プロトコル)] の略称です。3つの言葉の頭文字を合わせて、OGP と称されています。


OGPはもともと、Facebook が策定した仕様です。今では Facebook だけではなく、TwitterやLINEなど、様々なSNSでも利用されるようになりました。


OGPを利用すると、リンクの元となるコンテンツにどのような情報が含まれているか、効率良く伝えることができます。



## 2. OGPの設定方法


```
<!DOCTYPE html>
<html lang="ja">
    <head>
        <meta charset="UTF-8">
        <!-- Open Graph Protocol の設定-->

        <meta property="og:title" content="新田章太のプロフィール" />
        <meta property="og:type" content="website" />
        <meta property="og:url" content="https://givery-technology.github.io/it-training/html-4/mycard/index.html" />
        <meta property="og:image" content="https://givery-technology.github.io/it-training/html-4/mycard/images/haru.jpg" />
        <meta property="og:site_name" content="新田章太のプロフィール" />
        <meta property="og:description" content="株式会社ギブリー取締役。エンジニアの市場価値を高めるために仕事をしています。CODEPREPというオンラインプログラミング学習サービスをつくっています。" />
        <!-- ここまで -->
```


### og:site_name
このコンテンツが含まれるウェブサイトの名前を記述しています。


### og:title
リンク元のコンテンツのタイトルを記述します。htmlの`<title>`タグとほぼ同じ情報であることが多いです。


### og:type
リンク元にはどんな種類のコンテンツが含まれているかを記述します。


#### website
```<meta property="og:type" content="website" />```  
ウェブサイトのTOPページに指定します。
#### article
```<meta property="og:type" content="artcle" />```  
ウェブサイトやブログのTOPページ以外のときに指定します。


一般的に、ウェブサイトやブログの場合は `article` と書くケースが大多数です。
og:typeには、他にも `place` や `music` など、スマホアプリで使うときに便利なタグも存在します。


### og:url
リンク元のURLを記述します。


#### 絶対パス（OK）
```<meta property="og:url" content="https://maximum80.com/simages/">```
#### 相対パス（NG）
```<meta property="og:url" content="/images/">```


### og:image
リンク元の内容を表す画像URLを指定します。ここに記述されたURLの画像が、SNS上でシェアされます。>


#### 絶対パス（OK）
`<meta property="og:image" content="https://maximum80.com/images/logo.jpg">`
#### 相対パス（NG）
`<meta property="og:image" content="/images/logo.jpg">`


### og:description
リンク元のコンテンツの概要を記述します。ここに記述された文章が、SNS上でシェアされます。



## 2. Facebookの設定


```
        <!-- Open Graph Protocol の設定-->
        <meta property="og:site_name" content="新田章太のプロフィール" />
        <meta property="og:type" content="article" />
        <meta property="og:url" content="https://givery-technology.github.io/it-training/html-4/mycard/index.html" />
        <meta property="og:image" content="https://givery-technology.github.io/it-training/html-4/mycard/images/haru.jpg" />
        <meta property="og:title" content="新田章太のプロフィール" />
        <meta property="og:description" content="株式会社ギブリー取締役。エンジニアの市場価値を高めるために仕事をしています。CODEPREPというオンラインプログラミング学習サービスをつくっています。" />
        <!-- ここまで -->

        <!-- Facebookの設定 -->
        <meta property="fb:app_id" content="120388268586719" />
```


### fb:app_id の設定
fb:appidは、FacebookにOGPを表示させるためには必須のプロパティとなります。  
fb:appid以外にもfb:adminsも使うことができます。ただし、fb:adminsの場合、adminIDという個人IDを使うことになるため、個人情報を晒しているようなものです。出来ればfb:app_idを使うほうが良いです。


### Debugger
[Facebook Debugger](https://developers.facebook.com/tools/debug/)



## 3. Twitter Cardの設定


```
        <!-- Open Graph Protocol の設定-->
        <meta property="og:site_name" content="新田章太のプロフィール" />
        <meta property="og:type" content="article" />
        <meta property="og:url" content="https://givery-technology.github.io/it-training/html-4/mycard/index.html" />
        <meta property="og:image" content="https://givery-technology.github.io/it-training/html-4/mycard/images/haru.jpg" />
        <meta property="og:title" content="新田章太のプロフィール" />
        <meta property="og:description" content="株式会社ギブリー取締役。エンジニアの市場価値を高めるために仕事をしています。CODEPREPというオンラインプログラミング学習サービスをつくっています。" />
        <!-- ここまで -->

        <!-- Facebookの設定 -->
        <meta property="fb:app_id" content="120388268586719" />
        <!-- Twitter Cardの設定-->
        <meta name="twitter:site" content="@maximum_80" />
        <meta name="twitter:card" content="summary" />

```


Twitter CardsとはURLを含んだツイートに、そのページのタイトル・概要・アイキャッチ画像（サムネイル）を表示させる仕組みです。


### twitter:card
twitter:cardは、twitterでOGPを表示させるときの表示タイプを指定します。


#### content="summary"
最も一般的な表示形式です。
#### content="summarylargeimage"
Summaryカードの画像がより大きく表示される、形式的にはFacebookのOGPに近いタイプのカードです。


#### content="photo"
画像が優先して表示されるタイプです。画像をクリックするとツイート内容が表示されます。
ビジュアル訴求が重要な業種（アパレルや飲食店等）にオススメです。
#### content="gallery"
一度の投稿で複数枚の画像を表示させることができるカードです。
表示させる画像は最大4枚まで選択することができます。


#### content="app"
アプリを紹介する際に利用したいカードです。
アプリケーションの名前や紹介文、アプリアイコンだけでなく、評価や価格なども表示されます。


### Twitter Card Calidator
[Twitter Card Validator](https://cards-dev.twitter.com/validator)
