FROM node:18.16.0
RUN mkdir /code

# Copy codebase
COPY . /code

WORKDIR /code

ADD frontend/package.json /code/
COPY frontend/public/ /code/public
COPY frontend/src/ /code/src
RUN npm install

CMD ["npm", "start"]