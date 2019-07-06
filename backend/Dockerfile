FROM python:3.6-alpine

ENV PYTHONUNBUFFERED 1

COPY requirements.txt /tmp/
RUN pip install -q -r /tmp/requirements.txt -i https://mirrors.aliyun.com/pypi/simple

COPY . /app/
WORKDIR /app/

CMD ["/usr/local/bin/gunicorn", "backend.wsgi", "-b", "0.0.0.0:8000"]