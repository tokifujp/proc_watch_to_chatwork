# proc_watch_to_chatwork

watch some process in Linux server and notify Chatwork :)

## Usage

### manually

You can watch if destinated proccess is alive.

```
$ ./path/to/proc_watch.sh
```

### normally

You might wanna add it to your `crontab`:

```
*/1   *  *  *  *  cd /path/to/proc_watch_to_chatwork/ && ./proc_watch.sh
```

## Installations

Just a few environment variables :

1. `CHATWORK_ROOM_ID`: as you can read it, the ID of the Chatwork room you want it to post to.
2. `CHATWORK_APP_TOKEN`: also you'll need to get the Chatwork App Token.
3. `TARGET_NAME`: name of the target process ex: `sidekiq`
4. `TARGET_RECOVERY_COMMAND`: recovery command when `TARGET_NAME` is dead.  Leave blank if you do not require to recover.

Please configure above variables in the `.env` file.  You can `cp .env.sample .env && vim .env` to
configure :)
