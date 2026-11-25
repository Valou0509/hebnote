FROM node:20-bookworm
WORKDIR /wiki
RUN wget https://github.com/Requarks/wiki-v2/releases/latest/download/wiki-js.tar.gz \
&& tar xzf wiki-js.tar.gz -C/wiki \
&& rm wiki-js.tar.gz \
&& mkdir -p /wiki/data
RUN npm rebuild sqlite3
COPY config.yml /wiki/config.yml
EXPOSE 3000
CMD ["node", "server"]
