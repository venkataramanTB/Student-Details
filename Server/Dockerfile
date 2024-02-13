COPY package*.json ./

COPY ./ ./

RUN npm install \
    && npm install -g nodemon \
    && chmod +x /app/wait-for-it.sh

EXPOSE 5000

CMD [ "/app/wait-for-it.sh", "db:5432", "--", "nodemon", "index.js" ]