FROM python:3.7

RUN pip install fastapi uvicorn jinja2 aiofiles

EXPOSE 8090

COPY ./files /app

WORKDIR /app

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8090"]