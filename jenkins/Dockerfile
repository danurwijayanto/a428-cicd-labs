FROM node:16-buster-slim

# Set Timezone
ENV TZ=Asia/Jakarta
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Setting working directory. All the path will be relative to WORKDIR
WORKDIR /usr/src/a428-cicd-labs

# Installing project files
COPY ../ ./
RUN npm install

# Building app
RUN npm run build

# Running the app
CMD ["npm", "start"]
