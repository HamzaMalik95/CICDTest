# Set the base image to use for the container
FROM nginx:alpine

# Copy your HTML, CSS and JavaScript files into the container
COPY index.html /usr/share/nginx/html/
#COPY style.css /usr/share/nginx/html/
#COPY script.js /usr/share/nginx/html/

# Expose port 80 to allow traffic to the container
EXPOSE 80

# Start the nginx web server to serve the HTML, CSS and JavaScript files
CMD ["nginx", "-g", "daemon off;"]

