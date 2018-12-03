# New Modification

TipBotStellar main features: 
* Deposit XLM and token (MEMO required) 
* Tip XLM or token based stellar
* Check Balance
* Withdraw

# Usage
* Help : @TipBotStellar my balance
* List Token: @TipBotStellar list token
* Check Balance: @TipBotStellar my balance
* Withdraw: @TipBotStellar withdraw [amount] [xlm_or_token] [stellar_wallet_address] [memo]
- example: @TipBotStellar withdraw GCK3HDQJZNQYVI6QRGZ22D5GXRUUAFHUDT6HXKQBUPSUDZWJOEEXASCI MEMO
* Send Tip: Reply and Mention to @TipBotStellar [amount] [xlm_or_token]
- example: @TipBotStellar 1 BOT

# Deposit
To deposit or reload your wallet please send XLM or stellar supported token (CMA, XCN, USD, BTC, SLT, ETH, MOBI, EURT, RMT, XRP, HKDT, LTC, BCH, SBD, BTX, ALEXA, BOT) to 👇

GCD737UUDTTXF5MW3SLKLTV6BSZO27XUE62SPUX7P3AKQHHO2ZQMITIP

with TEXT MEMO: twitter/your_twitter_username


# Stellar Tipping bot

The stellar tip bot is there to thank people for help, be friendly, buy someone a coffee and spread the word about the amazing stellar network.

Here are a few features we want to highlight:

- *almost* instant deposit and withdrawals
- anonymous deposits
- easy and cross plattform tipping (reddit, twitter)
- on-platform balance checks
- fast free tipping
- automatic account funding for withdrawals > 1 XLM

Try it out!

## Use

You can use the stellar bot on [reddit](https://www.lumenauts.com/tutorials/how-to-tip-with-the-stellar-subreddit-tipping-bot) and [twitter](https://twitter.com/xlm_bot)!

Check:

- [a community made tutorial for reddit](https://www.lumenauts.com/tutorials/how-to-tip-with-the-stellar-subreddit-tipping-bot)
- [a community made tutorial for twitter](https://www.lumenauts.com/tutorials/how-to-tip-with-the-lumen-twitter-tipping-bot) and a great [twitter walk through on youtube](https://www.youtube.com/watch?v=MXZF0RY8D20&feature=youtu.be)

## Setup

Check out the repo and install dependencies:

```
npm install
```

Fire up a postgres container and create two databases:

```
docker run -itd --name db -p 5455:5432 postgres:latest
docker exec -ti db sh -c 'su postgres -c "createdb stellar"'
docker exec -ti db sh -c 'su postgres -c "createdb stellar_testing"'
```

Create an `.env` file:

```
MODE=development

PG_USER=postgres
PG_HOST=localhost
PG_PORT=5455
PG_NAME=stellar
PG_PASSWORD=

STELLAR_HORIZON=https://horizon-testnet.stellar.org
STELLAR_SECRET_KEY=YOUR_SECRET_KEY_HERE

REDDIT_CLIENT_ID=YOUR_REDDIT_APP_CLIENT_ID
REDDIT_CLIENT_SECRET=YOUR_REDDIT_APP_SECRET
REDDIT_USER=YOUR_STELLAR_BOT
REDDIT_PASS=YOUR_STELLAR_BOT_PASSWORD
REDDIT_SUBREDDITS=stellar,stellartutorials

TWITTER_USER=YOUR_TWITTER_USERNAME
TWITTER_API_KEY=YOUR_TWITTER_API_KEY
TWITTER_SECRET_KEY=YOUR_TWITTER_SECRET_KEY
TWITTER_ACCESS_TOKEN=YOUR_TWITTER_ACCESS_TOKEN
TWITTER_ACCESS_SECRET=YOUR TWITTER_ACCESS_SECRET

```

Create an `.env.test`:

```
MODE=testing

PG_USER=postgres
PG_HOST=localhost
PG_PORT=5455
PG_NAME=stellar_testing
PG_PASSWORD=

REDDIT_SUBREDDITS=foo,bar,baz
```

## Get it going

Run the tests:

```
npm run test
```

Run the app:

```
npm run app
```

## Contribute

We are always looking for contributors. A nice way to contribute is [creating more adapters](https://github.com/shredding/stellar-bot/wiki/How-To:-Create-an-adapter) on top of the bot.

## Donate

If you want to support the development of the bot, please send XLM to:

`GC2BDQ6BCDCIYLPHFGZKO4DJ3L3LQ4KTG3IZYF4M4UDBC3V2CZBZH3TU`

Thank you very much!

Enjoy.
