# LA Web サービスコース Day1 確認テスト<br>カウントアプリを 0 から構築し、追加機能を実装せよ

## レギュレーション

- 制限時間 30 分
- 順番に行う必要はありません．できる問題をできるだけ進めてください
- 講師への質問はできません
- このレポジトリを fork して clone し，実装を進め，制限時間内に commit してください
- push はテスト終了後に全員同じタイミングで行います．

## 開発の準備

- 現在のパスが`~/environment/` であることを確認
- `git clone <各自のレポジトリURL>` 各自の URL は GitHub の右上の緑色の箇所から確認できます
- `cd 確認テストのディレクトリ名`で移動
- `rake db:create`, `rake db:migrate`を入力して DB を準備
- `ruby app.rb` と入力してちゃんと起動するか確認(できなかったら講師を呼んでね！)

## commit のやり方

- `git add -A`
- `git commit -m "Implement feature: creating new counter"`

## 提出のやり方

- `git push origin main`

## 要件

### データベース

`counts`テーブル
| 型 | 内容 |
| :---: | :--- |
| 整数型 | カウンターの数字 |
| 日時型 | タイムスタンプ |

- model は構築済み
- カラム名は問いません

### ビュー

- index.erb
  - 数字・ラベルを表示

### コントローラ

- app.rb
  - カウンターの作成，更新

## 要求物

### レベル 0 : Sinatra の基礎の理解の確認

#### ノーマルなカウントアプリ

カウンターが一つ表示され，プラスボタンを押すとカウントアップされる  
<img src="https://image.docbase.io/uploads/5f0f4151-cfb1-4c7b-a39f-b94ced75c180.png">

### レベル 1 : HTML/CSS，ルーティングの基礎の確認

#### マイナスボタン

マイナスボタンを追加し，クリックするとカウントダウンされる  
<img src="https://image.docbase.io/uploads/9472cf09-7d02-4370-84d8-4f60e19a6cf6.png">

#### クリアボタン

クリアボタンを追加し，クリックするとカウンターの数字が 0 になる  
<img src="https://image.docbase.io/uploads/2c032741-f65b-428f-ac31-2e054e1b1387.png">

#### ×2 ボタン，÷2 ボタン

×2 ボタンを追加し，クリックするとカウンターの数字を 2 倍になる  
÷2 ボタンを追加し，クリックするとカウンターの数字が 2 で割った数になる
奇数の場合，小数点は切り捨てでよい  
<img src="https://image.docbase.io/uploads/4c66a69e-8ac0-470c-8b9c-3a154cbb62f3.png">

### レベル 2 : ルーティング，データベースの基本の確認

#### カウンターを増やす

2 つめのカウンターを作成，表示する  
2 つのカウンターは別々に動く  
<img src="https://image.docbase.io/uploads/d9c8a378-279c-4f76-8612-ea65653e0e9a.png">

2 つめのカウンターに実装するのプラスボタンのみでよい  
それ以外の機能を実装した場合は BONUS として扱う

### レベル 3 : ルーティング，マイグレーション，rake コマンドの基本の確認

#### カウンターに見出しをつけ，任意に変更できるようにする

カウンター上部に見出しとフォームを追加する  
フォームを送信すると見出しが更新される．  
リロードしても，この見出しは消えない．  
<img src="https://image.docbase.io/uploads/30466a50-1b2f-4aba-b252-bfb85f47940f.png">

見出しはフォームの入力欄に表示しても，フォームと別で表示してもどちらでもよい

### レベル 4 : MVC の基本の確認

#### カウンターを新しく作れるようにする

ページ上部にフォームを追加する  
見出しを入力し，フォームを送信すると入力した見出しがついたカウンターが新しく作成される  
すべてのカウンターは別々に動作する  
<img src="https://image.docbase.io/uploads/e28aa0d9-6dee-4099-bf82-65d9bd9498a7.png">

カウンターの表示される順番は問わない
2 つめのカウンターに実装するのプラスボタンのみでよい  
それ以外の機能を実装した場合は BONUS として扱う

## 配点

50 点満点です
配点は以下の通りです．

| ID  | 達成項目                                   | 点数  |
| :-: | :----------------------------------------- | :---: |
|  1  | ノーマルなカウントアプリ                   |   5   |
|  2  | マイナスボタン                             |   5   |
|  3  | クリアボタン                               |   5   |
|  4  | ×2 ボタン，÷2 ボタン                       |   5   |
|  5  | カウンターを増やす                         |  10   |
|  6  | カウンターに見出しをつけ，任意に変更できる |  10   |
|  7  | カウンターを新しく作成できる               |  10   |
|  8  | LGTM (いいね！とおもったらボーナス 1 点)   | BONUS |

### LGTM の基準

みず&がっしーがｲｲﾈ!とおもったこと．  
例えば

- 要求以上の機能ができている
- インデントが綺麗に揃っている
- スマートな実装
- デザインの工夫
  など．
