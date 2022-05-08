# Intial Deploy to heroku
Intially I was not able to push a simple bot to heroku, but yeah googling a lot made it work!

## Very Initial Steps [NOOB Steps]
1. Install Telegram :)
2. Create a telegram bot by talking to [Bot Father](https://t.me/botfather)
3. Install python in your computer, if you are on windows follow [this](https://www.python.org/downloads/windows/)
4. Install git, follow [this](https://git-scm.com/download/win)
5. Install Heroku account [here](https://signup.heroku.com/login)
6. Install Heroku CLI from [here](https://devcenter.heroku.com/articles/heroku-cli)
7. Install editor of your choice, I preffer [Atom](https://atom.io)

### Step 1:

- Just git clone this repository and start working by editing the code
   ```shell
   git clone https://github.com/DARKEMPIRESL/telegram-bot-heroku-deploy.git
   cd telegram-bot-heroku-deploy

### Step 2:
- Change directory to where you have made these files
- now in git bash CLI, intialize a git
  ```shell
  git init
  
### Step 3:
- Now install heroku CLI
- Next
  ```shell
  heroku login
  heroku create app_name
- If you have already created app then select it:
  ```shell
  heroku git:remote -a app_name
- Or else continue:
  ```shell
  git add -f bot.py Procfile requirements.txt __init__.py
- ```shell
  git commit -m "Added Files"
- Push files to heroku:
  ```shell
  git push heroku master
- If it is not working then try this one:
   ```shell
   git push heroku master --force
### At this point your bot should be running, you can check by
-  ```shell
    heroku ps
If it is not running then we have to reset dynos:
- ```shell
  heroku ps:scale worker=0
- ```shell
  heroku ps:scale worker=1
Now it should be running fine! Enjoy :)  

### If you are trying to lazy which you should not! (Deploying to Heroku)

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/DARKEMPIRESL/telegram-bot-heroku-deploy/blob/master)

Choose App name and deploy!
Follow from Step 7 and edit bot.py with your token!
And finally deploy!

### Want a video tutorial?
- Check It [Here!](https://github.com/DARKEMPIRESL/telegram-bot-heroku-deploy/issues/1)
