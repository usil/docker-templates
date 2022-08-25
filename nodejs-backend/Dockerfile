FROM node:14

RUN mkdir /usr/app
WORKDIR /usr/app
COPY . /usr/app
RUN npm install --only=prod
# build if it is required
# RUN npm run build

COPY DockerfileEntryPoint.sh /usr/local/bin/DockerfileEntryPoint.sh
RUN chmod 744 /usr/local/bin/DockerfileEntryPoint.sh

ENTRYPOINT ["DockerfileEntryPoint.sh"]
