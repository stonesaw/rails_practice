# rails practice

rails 勉強用 repo

こちらの [パーフェクト Ruby on Rails](https://www.amazon.co.jp/dp/4297114623/) という書籍が届くまで  
[Rails ガイド](https://railsguides.jp/getting_started.html?version=6.1) というサイトで勉強したことまとめ

---

(Slack から 自分用メモ)
## やったこと
- インストールした
    - rvm (on WSL 2)
    - ruby 2.6.9p207 (2021-11-24 revision 67954) [x86_64-linux]
    - Rails 6.1.4.6
    - node.js, yarn, sqlite3 はインストール済み だった
- テンプレ作成 `rails new <name>`
- ルーディング config/routes.rb
- コントローラーの追加 `bin/rails generate controller Articles index --skip-routes`

- 複数の記事をリスト 表示 / 記事の内容を表示
- 記事の作成 / 編集
- コメント機能 (2つ目のモデル)
- `bin/rails generate model Comment commenter:string body:text article:references`
- `bin/rails db:migrate`
- 子: `belongs_to` / 親: `has_many` でモデル同士の関連付け (`rails generate model` のオプションで自動追加 )
- コメントの追加
- マイグレーションとは
- concern を使うとモデルの共通化が出来る
- コメントの削除 / 記事の削除
- Basic 認証

## To Do
- `*_path` や `*_id` の理解が曖昧
- heroku にデプロイするために PostgreSQL に移行

erb 書式  
`<% ~ %>` は値を返さない (表示しない)  
`<%= ~ %>` は値を返す (表示する)  


<br>

---

<details>
<summary><h3>This README would normally document whatever steps are necessary to get the
application up and running.</h3></summary>

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

</details>