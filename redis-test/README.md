### This file contains basic Redis commands and a little example of how to use them.

---

## How to run

[Install Redis](https://redis.io/download) (Windows does not officially supports Redis, use WSL-Windows Subsystem Linux to install and run Redis server)

Open the redis-test folder, and start Redis server

```bash
redis-server
```

If you want to work on Redis CLI:

```bash
redis-cli
```

Run web server:

```bash
npm start
```

Now your Redis database and the web server are ready. By using Postman you can send GET requests to:

```bash
http://localhost:3000/photos
http://localhost:3000/photos/1
http://localhost:3000/photos/2
http://localhost:3000/photos/?albumId=1
http://localhost:3000/photos/?albumId=2
```

---

## Stats

|   Request Type    | Without Redis | With Redis |
| :---------------: | :-----------: | :--------: |
|      photos       |    512 ms     |   21 ms    |
|     photos/1      |     178ms     |    4 ms    |
| photos/?albumId=1 |    460 ms     | 4 seconds  |

As you can see using Redis boost the performance of project.
