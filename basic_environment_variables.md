# Basic Environment Variables
We don't want to publish logins, passwords, keys, tokens, client IDs, or other credentials and private information.

We can save these values in memory using environmental variables.

## Linux 

To save an environment varable named SECRET_KEY with a value of 1234567890 you can run the following command in a terminal window:
```
$ export SECRET_KEY="1234567890"
```

See if it's saved in memory by running:
```
$ echo $SECRET_KEY
```

To load environment variables on boot-up you need to save them in /etc/environment on Ubuntu 20.04 and most other linux distros.
```
$ sudo vi /etc/environment
```


## Python

To retrieve environment variables in a Python application you can use the [Python os interface](https://docs.python.org/3/library/os.html)

```
import os
.
.
.
SECRET_KEY = os.environ["SECRET_KEY"]
```
