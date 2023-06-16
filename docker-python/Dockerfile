FROM docker pull kalilinux/kali-rolling
FROM python:3
USER root

RUN apt update
RUN apt-get update
RUN install -y python3.11
RUN apt install -y python3-pip

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
RUN python3.11 -m pip install -r requirements.txt

WORLIR /usr/src/app

ADD --chown=user:group

COPY script.py .
ENTRYPOINT ["python3.8", "script.py"]
CMD [ "python", "./your-daemon-or-script.py" 