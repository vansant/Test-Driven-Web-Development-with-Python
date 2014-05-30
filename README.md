Test-Driven-Web-Development-with-Python
=======================================
<pre>
Setup
1. Python 3 Virtualenv
2. (Python3-venv)$ pip install django selenium
3. Download Firefox

Issues from May 29, 2014
1. Not working - pip install django==1.7 and pip install https://github.com/django/django/archive/stable/1.7.x.zip
2. Selenium assumes Firefox.app in /Applications on OS X by default
3. db.sqlite is referenced before it is created with python manage.py syncdb 

Solutions from May 29, 2014
1. pip install django - installed version 1.6.5
2. Python3-venv/lib/python3.4/site-packages/selenium/webdriver/firefox/firefox_binary.py
   def _get_firefox_start_cmd(self):
    """Return the command to start firefox."""
    start_cmd = ""
    if platform.system() == "Darwin":
        start_cmd = ("/set/path/to/Firefox.app/Contents/MacOS/firefox-bin")
3. Ignored knowing this file will be created later.

</pre>