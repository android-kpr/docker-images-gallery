FROM python:3.12.8

WORKDIR /app

EXPOSE 5050

COPY Pipfile Pipfile.lock ./

RUN pip3 install pipenv -i https://pypi.org/simple
RUN pipenv requirements > requirements.txt
RUN pip install -r requirements.txt

COPY . ./

CMD ["python", "main.py"]