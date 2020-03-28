## Validator Health Monitoring Bot

### Getting Started

```bash
git clone git@github.com:chris-remus/chainflow-icf-validator-tool-grant.git chainflow-icf-validator-tool-grant
cd chainflow-icf-validator-tool-grant/alert-bot
git checkout bot-alpha
cp example.config.toml config.toml
```

- To **Get Validator Status Alerts** populate *alert_time1* and *alert_time2* in `config.toml` in the form of UTC(ex:"02:25PM")
- For **Telegram Alerting** populate *chat_id* and *bot_token* in `config.toml` with your values
- For **Email Alerting** populate *token* and *to_email* (your email) in `config.toml` with your values

Start the bot service

```bash
$ go get .
$ go build main.go
$ ./main
```

Using docker
```sh
docker build -t cfv .
docker run -d --name validator-tg-bot cfv
```