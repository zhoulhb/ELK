FROM node:16.14-alpine

RUN apk add --no-cache git

WORKDIR /home/theia

RUN git clone https://github.com/eclipse-theia/theia.git && \
    cd theia && \
    yarn && \
    yarn theia build

EXPOSE 3000

CMD ["yarn", "theia", "start", "/home/theia", "--hostname=0.0.0.0"]
