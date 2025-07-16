# Crop links and get click statistics using VK API

The script transforms full-length URL like _https://google.com_ into short VK format [_9DUlSG_](https://vk.cc/9DUlSG)
and displays statistics on clicks for short links.

## How to install

Clone repository to your local device. To avoid problems with installing required additinal packages, its strongly to use a virtual environment [virtualenv/venv](https://docs.python.org/3/library/venv.html), for example:

```bash
python3 -m venv myenv
source myenv/bin/activate
```

Python3.12 should be already installed. Then use pip (or pip3, if there is a conflict with Python2) to install dependencies:

```bash
pip install -r requirements.txt
```

The script uses additinal packages:

requests==2.20.1

dotenv==0.9.9

After all these manipulations you can run script using something like this:

```bash
python3 main.py URL
```

As result you will see shorted link for full URL or statistics of clicks for short link.

In the script, for safety reasons, environment variables are used to restrict access for credentias, such as vk_token.
The file with the contents of these variables isnt included in the repository. To use the script with your credentials, you need to create an .env file in the folder with the script, and add into it lines like VK_ACCESS_TOKEN=your_token.

## Project Goals

The code is written for educational purposes on online-course for web-developers dvmn.org.
