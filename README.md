# todo-rails
---

# 参考サイト
https://reasonable-code.com/rails-todo/

## 概要
- シンプルtodo
- タスクの追加・編集・削除ができる
- tasksのcontrollerやview、modelを中心とした構成

## トラブルシューティング
- webpack未コンパイル問題
```
Webpacker::Manifest::MissingEntryError in Tasks#index
Showing /root/todo-rails/app/views/layouts/application.html.erb where line #10 raised:

Webpacker can't find application.js in /root/todo-rails/public/packs/manifest.json. Possible causes:
1. You want to set webpacker.yml value of compile to true for your environment
   unless you are using the `webpack -w` or the webpack-dev-server.
2. webpack has not yet re-run to reflect updates.
3. You have misconfigured Webpacker's config/webpacker.yml file.
4. Your webpack configuration is not creating a manifest.
Your manifest contains:
{
}
```
対応：
`rails webpacker:install`
`rails webpacker:compile`