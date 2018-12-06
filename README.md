# New Modification

TipBotStellar main features: 
* Deposit XLM and token (MEMO required) (deposit info send via direct message)
* Tip XLM or token based stellar
* Check Balance (balance info send via direct message)
* Withdraw (support withdrawal with MEMO and create new wallet)

# Usage
Create tweet and mention to @TipBotStellar

* Help 
```
@TipBotStellar help
```
* List Token
```
@TipBotStellar list token
```
* Check Balance
```
@TipBotStellar my balance
```
* Withdrawal : @TipBotStellar withdraw [amount] [xlm_or_token] [stellar_wallet_address] [memo]
```
@TipBotStellar withdraw 10 XLM GCK3HDQJZNQYVI6QRGZ22D5GXRUUAFHUDT6HXKQBUPSUDZWJOEEXASCI MEMO
```
* Send Tip: Reply to user you want to send tipping and mention to @TipBotStellar [amount] [xlm_or_token]

*For reply format
```
@TipBotStellar 1 XLM
```

*For fresh tweet format
```
@UserYouWantToSendTip 1 XLM @TipBotStellar [comment if available]
```


# Deposit
To deposit or reload your wallet please send XLM or stellar supported token (CMA, XCN, USD, BTC, SLT, ETH, MOBI, EURT, RMT, XRP, HKDT, LTC, BCH, SBD, BTX, ALEXA, BOT) to 👇

```
tipbot*stellarx.com 
```

wallet address

```
GCD737UUDTTXF5MW3SLKLTV6BSZO27XUE62SPUX7P3AKQHHO2ZQMITIP
```

with TEXT MEMO: twitter/your_twitter_username

# Supported XLM and Stellar Token (asset code and issuer)
```
XLM : native
CMA : GBWZHAVWY23QKKDJW7TXLSIHY5EX4NIB37O4NMRKN2SKNWOSE5TEPCY3 (cryptomover.com)
XCN : GCNY5OXYSY4FKHOPT2SPOQZAOEIGXB5LBYW3HVU3OWSTQITS65M5RCNY (fchain.io)
USD : GBSTRUSD7IRX73RQZBL3RQUH6KS3O4NYFY3QCALDLZD77XMZOPWAVTUK (stronghold.co)
BTC : GBSTRH4QOTWNSVA6E4HFERETX4ZLSR3CIUBLK7AXYII277PFJC4BBYOG (stronghold.co)
SLT : GCKA6K5PCQ6PNF5RQBF7PQDJWRHO6UOGFMRLK3DYHDOI244V47XKQ4GP (smartlands.io)
ETH : GBSTRH4QOTWNSVA6E4HFERETX4ZLSR3CIUBLK7AXYII277PFJC4BBYOG (stronghold)
MOBI : GA6HCMBLTZS5VYYBCATRBRZ3BZJMAFUDKYYF6AH6MVCMGWMRDNSWJPIH (mobius.network)
EURT : GAP5LETOV6YIE62YAM56STDANPRDO7ZFDBGSNHJQIYGGKSMOZAHOOS2S (tempo.eu.com)
RMT : GDEGOXPCHXWFYY234D2YZSPEJ24BX42ESJNVHY5H7TWWQSYRN5ZKZE3N (sureremit.co)
XRP : GCNSGHUCG5VMGLT5RIYYZSO7VQULQKAJ62QA33DBC5PPBSO57LFWVV6P (interstellar.exchange)
HKDT : GABSZVZBYEO5F4V5LZKV7GR4SAJ5IKJGGOF43BIN42FNDUG7QPH6IMRQ (cryptomover.com)
LTC : GC5LOR3BK6KIOK7GKAUD5EGHQCMFOGHJTC7I3ELB66PTDFXORC2VM5LP (apay.io)
BCH : GAEGOS7I6TYZSVHPSN76RSPIVL3SELATXZWLFO4DIAFYJF7MPAHFE7H4 (apay.io)
SBD : GB3KBOFUCVTWEZ7YIZ7PAKLQMKPCTGWU3LOMANMCT7V6I3AAK4USTEEM (steemanchor.com USD)
BTX : GBBAMI2WU6WJHDL3CQKT4LPXUC76WCEMQJMJIVQGL2G5IKJ2JHEVHG3G (bitx.tk)
ALEXA : GB5SDHWWW55EMY5IYREZ4XPSNDK3N6UTOYX2JQ7XEBHRZUTNK6OKVGGV (AlexaCoin.ID)
```


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

`GCD737UUDTTXF5MW3SLKLTV6BSZO27XUE62SPUX7P3AKQHHO2ZQMITIP`

Thank you very much!

Enjoy.
