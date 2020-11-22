# What image do you want to start building on?
FROM node:latest


# Make a folder in your image where your app's source code can live
RUN mkdir -p /src/app

# Tell your container where your app's source code will live
WORKDIR /src/app

# What source code do you what to copy, and where to put it?
COPY . /src/app

# Does your app have any dependencies that should be installed? // This installs all the dependencies necessary to run our node application using the yarn package manager
RUN yarn install

# What port will the container talk to the outside world with once created?
# This command will expose the container's port 3000 which will need to be mapped to a port on the host when spun into a container by using the -p option with the docker run command
EXPOSE 3000

# How do you start your app?
CMD [ "npm", "start" ]
