---
Author: Vlad Doster <mvdoster@gmail.com>
Date: 2020-07-01 17:54:50
Last Modified by: Vlad Doster <mvdoster@gmail.com>
Last Modified time: 2020-07-01 18:19:49
""
---

# Automate Registration of classes

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

3. Fill out `config.ini`

   Username and Password should be ones that you use to login to classes registration portal.
   **Tweakable settings**
   | Identifier | What it does                                |
   | ---        | ---                                         |
   | cycles     | How many time to run. -1 for infinite loop. |
   | wait_time  | Wait for N # of seconds between attempts    |

4. Run

```bash
# No logfile
python main.py > log.txt

# Generate log file
python main.py > log.txt
```
