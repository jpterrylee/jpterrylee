- 👋 Hi, I’m @jpterrylee
- 👀 I’m interested in ...learning ruby now.
- 🌱 I’m currently learning ruby rails
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
jpterrylee/jpterrylee is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

### Docker
Clone issue form Github: 
"git clone https://github.com/******/******"

First run:  [bundle install]
- docker-compose run web bundle install

Install yarn: [yarn install]
"Please run `yarn install --check-files` to update. と言われたら"
- docker-compose run --rm web yarn install --check-files

###  最初のセットアップ
- docker-compose build
- docker-compose run --rm web bin/setup

## racc エラーの場合
docker-compose run web gem install racc -v ‘1.6.0’ --source ‘https://rubygems.org/’


### もしtestDBがない場合は
- docker-compose run --rm web bin/rails db:create RAILS_ENV=test
- docker-compose run --rm web bin/rails db:migrate RAILS_ENV=test

###  seedデータの投入（不要）
docker-compose run --rm web bin/rails db:seed_fu

###  サーバー起動
docker-compose run --rm --service-ports web


###  workerの起動
docker-compose run --rm --service-ports worker

###  rspecの実行
docker-compose run --rm web bundle exec rspec

###  rubocopの実行
docker-compose run --rm web bundle exec rubocop

###  html hamlの実行
docker-compose run --rm web bundle exec haml-lint app/views/

### brakemanの実行
docker-compose run --rm web bundle exec brakeman

### brakemanの実行
docker-compose run --rm web bundle exec rails_best_practices -e node_modules
```

vim 
How to install on macOSX 10.14
1. go to https://formulae.brew.sh/formula/vim to copy "brew install vim" paste to terminal and hit[enter]
2. export PATH="/usr/local/bin:$PATH" > copy paste to terminal and hit [enter]


```
///////////

How to install Typescript on mac
sudo npm install -- global typescript

uninstall:
sudo npm uninstall --global typescript

///////////
