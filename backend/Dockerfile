# Specify the Platform or infrastructure to use
FROM node:16-alpine 

# Specify the working directory or the location of our app
WORKDIR /usr/app/

# Copy the package to the working directory
COPY ./package.json .

# Install all the packages
RUN npm install

# and then copy everything to the working directory
COPY . .

EXPOSE 8000

# Specify the run function
CMD [ "npm", "start" ]

# ? Question: Why copy package.json first, install next and last start 
# ! Because if we re run docker it will first check if package.json - 
# ! is changed then does the next. so we need to 