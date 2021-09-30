# Heroku startup settings
請先到Heroku官網註冊帳號，並依照步驟將Django專案部屬到Heroku。

## 環境
- Ubuntu 16.04

## 開發套件
- django
- django-heroku
- gunicorn

## 安裝Heroku
```
sudo snap install heroku --classic
```
其他作業系統的安裝方式，請參考
https://devcenter.heroku.com/articles/heroku-cli#download-and-install


## Quick Start
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/chenuin/heroku-startup-settings/tree/master)
請先註冊 Heroku 帳號，點選按鈕即可快速將 Github 專案部屬到 Heroku


## 說明
將範例專案下載到你的電腦
```sh
git clone https://github.com/chenuin/heroku-startup-settings.git
```


#### Step1. 登入Heroku
若安裝heroku cli後，請用Heroku申請的帳號密碼登入。
```sh
heroku login
```


#### Step2. 建立新專案
請在`<project-name>`填入自訂的專案名稱。
```sh
heroku create <project_name>
heroku git:remote -a <project_name>
```
假設專案名稱為`myproject`，打開瀏覽器`myproject.herokuapp.com`查看你的專案，因此如果顯示"Name `<project-name>` is already taken"，可能是你想要的名稱已經先被佔用了，只要換別的名字試試看就好了。


#### Step3. 上傳
```sh
heroku config:set DISABLE_COLLECTSTATIC=1
git push heroku master
heroku ps:scale web=1
```


#### Step4. 查看網站
只要打開`https://<project_name>.herokuapp.com/`，就可以看到結果囉！如果不記得專案名稱，可以透過指令顯示執行網站url。
```
heroku open
```
範例專案的建立過程請參考：
https://chenuin.blogspot.com/2018/08/django-djangoheroku.html


