# proc_watch_to_chatwork

watch some process in Linux server and notify Chatwork :)

## Usage

### manually

You can watch if destinated proccess is alive.  Below is an example of watching `sidekiq`:

```
$ ./path/to/proc_watch.sh sidekiq
```

### normally

You might wanna add it to your `crontab`:

```
*/1   *  *  *  *  cd /path/to/proc_watch_to_slack/ && ./proc_watch.sh sidekiq
```

## Installations

Just a few environment variables :

1. `CHATWORK_ROOM_ID`: as you can read it, the ID of the Chatwork room you want it to post to.
2. `CHATWORK_APP_TOKEN`: also you'll need to get the Chatwork App Token.

I think you don't wanna expose either of the above.
