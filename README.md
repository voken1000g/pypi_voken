# Python Packages from Voken

[![PyPi Version](http://img.shields.io/pypi/v/voken.svg)](https://pypi.python.org/pypi/voken/)
![Python Version](https://shields.io/badge/python-%5E3.8-blue)

Python Packages from Voken Project

## shell

Embed and provide a interactive console...

```python
from voken import shell

shell.embed('welcome')

# >>>
```


## text_link

- Extract all `TEXT_LINK(s)`
- Get `hostname` from a `TEXT_LINK`
- Get `telegram_username` from a `TEXT_LINK`

```python
from voken import text_link as tl

text = 'Lorem ipsum dolor sit amet, a.com b.com/a c.io c.io/abc t.me t.me/BotFather telegram.me telegram.me/BotFather something else...'

text_links = tl.find_all_text_links(text)
for text_link in text_links:
    print()
    print(text_link)
    print(tl.get_hostname(text_link))
    print(tl.get_telegram_username(text_link))

# a.com
# a.com
# None

# b.com/a
# b.com
# None

# c.io
# c.io
# None

# c.io/abc
# c.io
# None

# t.me
# t.me
# None

# t.me/BotFather
# t.me
# BotFather

# telegram.me
# telegram.me
# None

# telegram.me/BotFather
# telegram.me
# BotFather
```
