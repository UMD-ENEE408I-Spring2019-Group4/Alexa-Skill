# Alexa-Skill
Alexa Voice Menus and JSON requests

Based mostly on amazon's flask-ask [tutorial](https://developer.amazon.com/blogs/post/Tx14R0IYYGH3SKT/Flask-Ask:-A-New-Python-Framework-for-Rapid-Alexa-Skills-Kit-Development)


# To Set Up:
## Install Pip:
download here

## Install Flask-Ask:


## Install Ngrok

## Downgrade Cryptography:
install cryptography==2.2.4me.py



# To Run:
## Start the Application
In a terminal window, navigate to the directory that has the code and run

```python3 ./app.py```
## Open an ngrok channel
Open a new terminal window using `ctrl` `alt` `t`
then run

```./ngrok http 5000```
Leave this window open

## Point the skill to the channel
open alexa skill
update the default endpoint with the https://########.ngrok.io url displayed in the terminal next to "Forwarding" when you ran the `./ngrok http 5000` command
