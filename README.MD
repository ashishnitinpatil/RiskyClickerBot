# [/u/RiskyClickerBot](http://reddit.com/u/RiskyClickerBot) for Reddit

A quick rundown of what the bot does is [here.](https://medium.com/@sreenivasvrao/introducing-u-riskyclickerbot-22b3d56d1e2a)

A more in-depth version, with a few code snippets is also [available.](https://medium.com/@sreenivasvrao/making-reddit-safer-for-work-with-u-riskyclickerbot-3bcb54fc1fe6)

# Getting Started

	git clone https://github.com/SreenivasVRao/RiskyClickerBot.git
	cd RiskyClickerBot
	pip install -r requirements.txt
 	
You will need to edit `vars.sh` to set the various environment variables. These values are retrieved by creating API keys.

For Reddit - go [here](https://www.reddit.com/prefs/apps/). [This tutorial](http://pythonforengineers.com/build-a-reddit-bot-part-1/) is a great start.

For Imgur  - Follow [this video](https://www.youtube.com/watch?v=OiDQu-0-DIA) - between the 4:00 and 6:00 minute marks, the video explains how to get the client id and secret which is all you need.

For Clarifai - [This article](http://blog.clarifai.com/introducing-api-keys-a-safer-way-to-authenticate-your-applications/) will help. I have set the scope to 'all' for my API key, although it can probably work with just the prediction scope.


Once you have the keys ready in `vars.sh`:

	. vars.sh

will load the variables in your current shell

Following that, you need to launch the bot:

	python bot.py

Running the bot on Heroku is possible by using the `--heroku` switch. However, Reddit usually frowns on duplicate bots. On the other hand, I'll gladly take pull requests for this bot. :)

# Acknowledgements
[praw](https://github.com/praw-dev/praw/) (c) 2016, Bryce Boe -  licensed under BSD 2-clause "Simplified" License
[imgurpython](https://github.com/Imgur/imgurpython)  (c) 2014 Imgur LLC - licensed under MIT license.
[clarifai](https://github.com/Clarifai/clarifai-python) (c) 2016 Clarifai, Inc. - licensed under Apache License, Version 2.0
[bmemcached](https://github.com/jaysonsantos/python-binary-memcached/) (c) 2011 Jayson Reis - licensed under MIT license.

