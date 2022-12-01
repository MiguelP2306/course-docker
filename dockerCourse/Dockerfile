# definimos la verision de node
FROM node:12

# copiamos primero esto y asi cada vez que se haga un cambio en el codigo no haga el install
COPY ["package.json", "package-lock.json", "/usr/src/"]

# nos movemos al directorio
WORKDIR /usr/src

# hacemos el install
RUN npm install

# ahora si copiamos todos los archivos del proyecto
COPY [".", "/usr/src"]

# exponemos el puerto por el cual la maquina afitriona puede acceder a este contenedor
EXPOSE 3000

# en caso de que no se ejecute un comando tenemos este por default
CMD ["npx", "nodemon", "index.js"]
