# Use the official NGINX base image
FROM nginx:latest

# Copy the HTML file into the NGINX default HTML directory
COPY webapp1-code/index.html /usr/share/nginx/html

# Optional: If you have additional static assets, copy them to the NGINX directory
# COPY static /usr/share/nginx/html/static

# Optional: Customize NGINX configuration if needed
# COPY nginx.conf /etc/nginx/nginx.conf

# Expose the default NGINX port
EXPOSE 80

# Start NGINX in the foreground
CMD ["nginx", "-g", "daemon off;"]
