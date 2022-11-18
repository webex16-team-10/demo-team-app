Notion
URL：https://www.notion.so/10-6196dab8eecc4471b544c3f55992bd89


【ターミナルコマンド】
- ①npm ci
    - ディレクトリにある node_module を完全復帰させるコマンド。
    - git clone した後、clone したディレクトリでする。
- ②npm run lint --fix
    - インデントを自動修正するコマンド
    - インデント：文章の行頭に空白を挿入して、先頭の文字を右に押しやること
- ③npm run serve
    - サーバーを立ち上げるコマンド。
    - 出てきた URL にアクセスすると、Web にコード内容が反映される。


【GitHub にアップロード＋ merge の手順】
- VScode で別ブランチに移動する
  - 「git branch ○○(ブランチ名)」⇒「git checkout ○○(ブランチ名)」
  - ※「git checkout -b ○○(ブランチ名)」で上記２つを同時に行える
  - ※「git branch」で作ったブランチを一覧化できる
  - ※「git branch -d ○○(ブランチ名)」でブランチを削除できる
- ファイルに変更したのち、「git add .」「git commit -m “コメント”」「git push origin ○○（ブランチ名)」
⇒GitHub にファイルがアップロードされた
- pull request からプルリクを出す
⇒Discord でもプルリクの通知が来る
- ほかの人がレビューをし、問題なければ merge する
  - [プルリクエストの内容をローカル環境で稼働確認する(github) - Qiita](https://qiita.com/great084/items/ad74dd064a2c2bc47cff)
⇒GitHub で、master ブランチが更新される
- 開発者の VScode に master ブランチの内容を反映させる
  - master ブランチに移動する
    - 「git checkout master」
  - 「git fetch」：github の内容をダウンロードする
  - 「git pull origin master」：ダウンロードしたファイルを反映させる


【開発の際に気を付けること】
- 必ず master ブランチ以外のブランチでやること
