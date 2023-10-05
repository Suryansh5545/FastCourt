FROM python:3.11

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1

#System Dependencies
RUN apt-get update

# Set work directory
RUN mkdir /code
WORKDIR /code

# Install dependencies
ADD requirements/* /code/
RUN pip install -r dev.txt

CMD ["./docker/wait-for-it.sh", "db:5432", "--", "sh", "/code/docker/dev/django/container-start.sh"]
