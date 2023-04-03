# Python-for-beginners_2
# creating modules
# module search path
from datetime import datetime, timedelta
import time
import json
from zipfile import ZipFile
from pathlib import Path
import HelloWorld
import sys

print(sys.path)
# using dir function
print(dir(HelloWorld))

print(HelloWorld.__name__)
print(HelloWorld.__package__)
print(HelloWorld.__file__)

# working with paths in python


Path(r"C:\Program Files\Microsoft")
path = Path("/usr/local/bin")
Path() / Path("/usr/local/bin")
Path.home()  # for the current user
print(path.name)
Path.exists
Path.is_dir
Path.is_file
print(path.stem)
print(path.suffix)
print(path.stat)
print(path.parent)
path = path.with_name("file.text")
print(path)
print(path.absolute)
path = path.with_suffix(".jpg")
print(path)
path = path.with_name("bin")
path = path.with_suffix("")
print(path)

# working with directories
path = Path("BSE Studies/Python by profession")
print(path)
# path.rmdir()
# path.mkdir()
# path.exists
# path.rename("Grow")
path.iterdir()
print(path.iterdir)
# paths= [p for p in path.iterdir() if p.is_dir()] ::: to find files in such directory
py_files = [p for p in path.glob("**/*.py")]
py_files = [p for p in path.rglob("*.py")]
print(py_files)
# print(path.stat())
# copying file
# source = Path("ecommerce/__init__.py")
# target=Path()/"__init__.py"
# to copy
# target.write_text(source.read_text())
# or
# import shutil
# shutil.copy(source, target)

zip = ZipFile("files.zip", "w")
for path in Path("PYTHON BY PROFFESSION").rglob("*.*"):
    zip.write(Path)
zip.close()
# woeking with json files
# working with timestamps


def send_emails():
    for i in range(10000):
        pass


start = time.time()
send_emails()
end = time.time()
duration = end-start
print(duration)
# working with date times

dt = datetime(2021, 4, 2)
dt = datetime.now()
dt = datetime.strptime("2023/04/02", "%Y/%m/%d")
dt = datetime.fromtimestamp(time.time())
print(f"{dt.year}/{dt.month}")
print(dt.strftime("%Y/%m"))
#working with time deltas
dt1=datetime(2021, 4, 2) + timedelta(days=2, seconds=2)
dt2=datetime.now()
duration=dt2-dt1
print(duration)
print("days", duration.days)
print("seconds", duration.seconds)
print("total_seconds", duration.total_seconds())

#generating randoms in python
import random
import string
print(random.random())
print(random.uniform(1, 2))
print(random.choice([1, 2, 3, 4]))
print(random.choices([1, 2, 3, 4, 5], k=3))
print(random.choices("xyzdadfv", k=4))
print("".join(random.choices(string.ascii_letters + string.digits, k=7))) #creation of password
print(string.digits)
#shuffle
numbers=[1, 2, 3, 4]
random.shuffle(numbers)
print(numbers)
#opening webbrowser
import webbrowser

print("deployment completed")
#webbrowser.open("http://google.com")
#send emails and templates
from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText
from email.mime.image import MIMEImage
import smtplib
from string import Template

##template=Template(path("template.html").read_text())
##template.substutute()



message=MIMEMultipart()
message["from"]= "Telesphore Uwabera"
message["to"]="telesphore91073@gmail.com"
message["subject"]="This is my first email via python!"
message.attach(MIMEText("Body"))
##Body=template.substitute({"name":"John"})
message.attach(MIMEText("Body", "html"))
message.attach(MIMEImage(Path("IMG-1411.jpg").read_bytes()))

with smtplib.SMTP(host="smtp.gmail.com", port=587) as smtp:
    smtp.ehlo()
    smtp.starttls()
    smtp.login("telesphore91073@gmail.com", "91073@Tecy")
    smtp.send_message(message)
    print("sent...")

#command in line arguments
import sys

if len(sys.argv)==1:
    print("USAGE: python3 app.py <password>")
else:
    password=(sys.argv)
    print("Password", password)
#running external directories
import subprocess


completed=subprocess.run(["python3", "other.py"], Capture_Output=True, text=True)
print("args", completed.args)
print("returncode", completed.returncode)
print("stderr", completed.stderr)
print("stdout", completed.stdout)
if completed.returncode !=0:
    print(completed.stderr)
