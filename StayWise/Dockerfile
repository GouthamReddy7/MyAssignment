# Use a base image with Node.js
FROM node:18

# Set the working directory in the container
WORKDIR /app

# Copy all necessary files and folders to the container
COPY . .

# Install dependencies for each project


RUN cd staywise && npm install
RUN cd Backend && npm install 

# Expose the necessary ports
EXPOSE 3000 5000

# Command to run the frontend and backend services in parallel
CMD ["sh", "-c", "cd Backend && nodemon server.js & cd staywise && npm start"]
