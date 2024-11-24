Create an app on Heeoku: bdbao-simple-flask-app
curl https://cli-assets.heroku.com/install.sh | sh
heroku login

gh auth login
gh repo create bdbao-simple-flask-app --public
git init
heroku git:remote -a bdbao-simple-flask-app
git remote add origin https://github.com/bdbao/bdbao-simple-flask-app.git
git add .
git commit -m "init: Initial commit"
git branch -M main
git push -u origin main


Lưu API key và tên ứng dụng vào GitHub Secrets:
    Vào repo trên GitHub > Settings > Secrets and variables > Actions.
    Thêm HEROKU_API_KEY (lấy từ heroku auth:token).
    Thêm HEROKU_APP_NAME (tên ứng dụng trên Heroku).

heroku auth:token
heroku apps

