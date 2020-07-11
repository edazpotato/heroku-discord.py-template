# heroku-discord.py-template
A template for people who want to use heroku with their discord.py projects.

## Instructions
1. clone this repo: `git clone https://github.com/edazpotato/heroku-discord.py-template.git`
2. replace the contents of [requirements.txt](/requirements.txt) with the dependecies for your project
3. stick your modiefied repo up on github, or use heroku CLI
4. if you used github, go to the heroku dashboard, create a new app (it's free!), and click *connect to github*
5. choose the repo you stuck your code in, click *enable automatic deploys*
6. now click on *Resources* in the navigation bar
7. you should see a box that says `worker python3 app.py`. On click on the edit icon to the very right of said box
8. now click the slider so that it is blue, then click *confirm*
9. you should now have a discord bot that runs 24/7 for free

## Notes
- If you want to use this with node.js, chnage the [Procfile](/Procfile) to say `worker: node myMainScript.js`
- If you want to have persistant user data, you will need to use an addon (which costs money) or have your databases hosted externaly since data does not persist between builds on heroku
- If you are storing your token, or something else in enviroment variables, you will need to go to `settings > reveal config vars` and add them there
- You shouldn't upload you token or any sensitve data to github, as anyone can see it
- You can change [runtime.txt](/runtime.txt) to have the version of python that your app is running on
