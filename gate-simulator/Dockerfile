FROM node:17

# Создать каталог приложений
WORKDIR /usr/src/app

# Объединить исходный код приложения
COPY . .

#Установка зависимостей приложения
#Подстановочный знак используется для обеспечения того,
#чтобы как package.json,
#так и package-lock.json копировались там, где это возможно (npm@5+)
#COPY package*.json ./

RUN npm install
# Если вы создаете свой код для производства, ЗАПУСКАЙТЕ npm ci --only=production

EXPOSE 9999

CMD [ "npm", "start" ]