# Crop links and get click statistics using VK API

The script transforms full-length URL like _https://google.com_ into short VK format [_9DUlSG_](https://vk.cc/9DUlSG)
and displays statistics on clicks for short links.


## How to install

Clone repository to your local device. To avoid problems with installing required additinal packages, its strongly to use a virtual environment [virtualenv/venv](https://docs.python.org/3/library/venv.html), for example:

```bash
python3 -m venv myenv
source myenv/bin/activate
```

## Environment

### Requirements

Python3.12 should be already installed. Then use pip (or pip3, if there is a conflict with Python2) to install dependencies:

```bash
pip install -r requirements.txt
```

The script uses additinal packages:

requests==2.20.1

dotenv==0.9.9

### Environment variables

- VK_ACCESS_TOKEN

1. Put `.env` file near `main.py`.
2. `.env` contains text data without quotes.

For example, if you print `.env` content, you will see:

```bash
$ cat .env
VK_ACCESS_TOKEN=v3.r.122857201.8f0cg543b36467ef22c8a234ae54290f700f836c.804fhh73cce5e8hgyr7n5c2397cgtracf570b7f2
```

#### How to get

* Register an application [API VK](https://dev.vk.com/ru) and get the `VK_ACCESS_TOKEN`

## Run

Launch on Linux(Python 3) or Windows:

```bash
python3 main.py URL
```

As result you will see shorted link for full URL or statistics of clicks for short link.
```bash
python main.py google.com
Сокращенная ссылка: https://vk.cc/9DUlSG
```

```bash
python main.py 9DUlSG
Количество просмотров: 269
```

## Notes

The file with the contents of these environment variables isnt included in the repository.

## Project Goals

The code is written for educational purposes on online-course for web-developers dvmn.org.
