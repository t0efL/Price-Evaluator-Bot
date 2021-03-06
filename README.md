# Price-Evaluator-Bot

**Telegram bot that predicts the price of clothing by an image [ENG].**

What is Price Evaluator Telegram Bot?
-----------------------------------------
Price Evaluator Telegram Bot is the final project for the Hackathon by ODS.

![alt text](https://github.com/t0efL/Price-Evaluator-Bot/blob/main/images/ods.jpg)

The goal was to create a telegram bot which can predict the price of clothing by an image. It was also necessary to deploy the bot to the server, so that the bot could run smoothly and not fall asleep.

The Bot itself: `@PriceEvaluatorBot` (Telegram)

It is possible that you found the bot by tag and found it not working. The reason most likely was that we stopped supporting the bot some time after it was created, so as not to waste the power of the server.

Idea
-----
We hope that this bot might help to motivate people sell their clothes instead of throwing out them. We think that this technology would work well as built-in in of the online stores like Avito. There is a lot of ways to improve it but the base is created.

Technology
-------
The bot is based on efficientnetb4. The weigths and the encoder we use in code are [here](https://drive.google.com/drive/folders/1mtsRFAt-K7MCR8En2qmsqSwjtti4RhAH?usp=sharing). You should download this folder and place it in your project repository avoiding changing name to use it. They are too large to place them here. We used the dataset from the [Avito Demand Prediction Challenge](https://www.kaggle.com/c/avito-demand-prediction) Kaggle competition. The simple pipeline for training is [here](https://github.com/t0efL/Price-Evaluator-Bot).

Bot
---
We chose [aiogram](https://docs.aiogram.dev/en/latest/index.html) as the main framework for writing the bot.

You can install it by the following command:

`$ pip install -U aiogram`

The main advantage of this framework over others is asynchrony. This allows processing requests from multiple users simultaneously. This framework supports webhooks as well as others, but we use regular polling instead, cause we have our own server, which allows the bot to work without falling asleep.

The entire code of the bot itself is located in the module [main.py](https://github.com/t0efL/Price-Evaluator-Bot/blob/main/main.py).

The bot can process some commands in the message and images, but it ignores the rest.

Setup
----------------
I set up the bot via `@BotFather`, and there I got an unique token for my bot.
Thanks to BotFather's capabilities, I was able to create a more comfortable environment for working with the bot. Here's what it looks like:

![alt text](https://github.com/t0efL/Price-Evaluator-Bot/blob/main/images/interface.jpg)

**Before running my code, make sure that you get your own token from BotFather and specify it in the file main.py.**

Deploy and additional files
---------------------------
As I already said above, we have our own server so we haven't done deploy on public server. If you want to create the same bot and deploy it on the server, but you don't have your own, check out my detailed tutorial [here](https://github.com/t0efL/Style-Transfer-Telegram-Bot). We've placed all the neсessary files for deploy on server (Procfile, requirements.txt, runtime.txt) in this repository, so you can take and use them for your deploy.

Team
--------
- Vadim Timakin
- Maksim Zhdanov
- Fyodor Dobryansky
- Yevhen Kravchenko
- Vladislav Lebyodkin
- Vyacheslav Chuev

License
----------
This project is released under the [Apache 2.0 license](https://github.com/t0efL/Price-Evaluator-Bot/blob/main/LICENSE).
