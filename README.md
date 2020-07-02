---
Author: Vlad Doster <mvdoster@gmail.com>
Date: 2020-07-01 17:54:50
Last Modified by: Vlad Doster <mvdoster@gmail.com>
Last Modified time: 2020-07-01 18:27:24

---

# Automate registration of classes

## Run:

1. Install dependencies via `requirements.txt`

```bash
python3 -m venv venv
source venv/bin/activate
python -m pip -r install requirements.txt
```

2. Install `chromedriver`

#### Linux:

```bash
# ubuntu
apt-get install chromedriver

# arch
sudo pacman -s chromedriver

# fedora/centos
sudo yum install chromedriver
```

#### MacOS:

```bash
brew install chromedriver
```

3. Fill out [config.ini](config.ini)

   Username and Password should be ones that you use to login to classes registration portal.
   **Tweakable settings**
   | Identifier | What it does                                |
   | ---        | ---                                         |
   | cycles     | How many time to run. -1 for infinite loop. |
   | wait_time  | Wait for N # of seconds between attempts    |

4. Run

```bash
./auto-register -h 
usage: auto-register [-h] [--verbose] [-l] 
Auto register for classes using supplied CRNs 
optional arguments: 
  -h, --help      show this help message and exit 
  --verbose, -v   Allow info and debug log messages. Useful if something is broken. 
  -l, --log-file  Log to a file in the current working directory. 
Created and maintained by Vlad Doster <mvdoster@gmail.com>
```
