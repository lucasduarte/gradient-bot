# Gradient network hang up script

- Project address: [https://app.gradient.network/](https://app.gradient.network/signup?code=N1HUDM)
- Buy proxy IP: [https://app.proxy-cheap.com](https://app.proxy-cheap.com/r/0CFUkV)

## Start with Docker

### Prepare proxy IP (optional)

Save the proxy address to proxies.txta file in the format:

> socks5://username:password@proxyhost:port

## Then start the container:

```bash
docker run -d -e APP_USER=user@mail.com -e APP_PASS=password -v ./proxies.txt:/app/proxies.txt overtrue/gradient-bot
```

Note：`proxies.txt` Please replace the path with the correct path. If there is no proxy, you can leave it blank, or `cd` go to `proxies.txt` the directory first and then execute the docker run command.。

## View the operation log

```bash
docker ps
```

This command will list all containers, find the corresponding container ID (the value corresponding to the "CONTAINER ID" column), and then execute: 

```bash
docker exec -it <container_id> pm2 logs
```

## Deleting a container

```bash
docker rm -f <container_id>
```

## 更新版本

```bash
# delete old container
docker rm -f <container_id>

# pull new image
docker pull overtrue/gradient-bot

# run new container
docker run -d -e APP_USER=<user@mail.com> -e APP_PASS='<password>' -v ./proxies.txt:/app/proxies.txt overtrue/gradient-bot
```

## Note

- Run this bot, and it will update your referrer code to my invite code if you don't have one.
- You can just run this bot at your own risk, I'm not responsible for any loss or damage caused by this bot. This bot is for educational purposes only.

## Contribution

Feel free to contribute to this project by creating a pull request.
