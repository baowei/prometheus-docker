FROM python:3.8.6-slim-buster
WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY views/ ./views/
COPY templates/ ./templates/
COPY app.py .

CMD [ "gunicorn", "app:app", "-b", "0.0.0.0:80"]