FROM node:10

RUN mkdir /home/node/.npm-global
ENV PATH=/home/node/.npm-global/bin:$PATH
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global

ENV HOME=/home/node

WORKDIR $HOME/app
RUN npm i -g npm
 
RUN npm install -g yarn

RUN rm -Rf /node_modules 
RUN yarn global add @angular/cli

RUN yarn install 

EXPOSE 4200

CMD [ "node" ]
