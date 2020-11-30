FROM python:latest

COPY . /app/

ENV POSTGRES_USER: "Richard"

ENV POSTGRES_PASSWORD: "mdp"

ENV POSTGRES_DB: "db"

ENV CSV_FILENAME: "data.csv"

RUN pip3 install psycopg2

RUN wget https://raw.githubusercontent.com/vishnubob/wait-for-it/master/wait-for-it.sh -P /

RUN chmod +x /wait-for-it.sh

ENTRYPOINT ["/wait-for-it.sh", "db:5432", "--"]

EXPOSE 5432

CMD ["python","-m","app"]