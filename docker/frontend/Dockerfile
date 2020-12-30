# pull official base image
FROM node:12.19

ENV DEBIAN_FRONTEND noninteractive

# set working directory
WORKDIR /app

#RUN yarn install --silent

# add app
#COPY package.json yarn.lock /app/

# expose api port
EXPOSE 3000

# yarn install
RUN yarn install

ENTRYPOINT ["/bin/bash", "/app/entrypoint.sh"]

CMD ["start"]
