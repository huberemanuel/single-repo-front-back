#build flask app
FROM python:3.10.12
RUN mkdir /app
WORKDIR /app
COPY ./requirements.txt /app/requirements.txt
RUN pip install --upgrade pip && \
  pip install -r requirements.txt

#RUN pip install python-dotenv
ENV FLASK_ENV production

COPY . .
EXPOSE 5000
CMD [ "gunicorn", "--bind", ":5000", "app:app"]