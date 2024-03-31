# Use nginx base image
FROM nginx

# Copy HTML files into the container
COPY index.html /usr/share/nginx/html/index.html

# Set environment variable for back-end URL
ENV WS_BACK_URL=http://backend-service:5000

# Use an entrypoint script
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]

# Expose port 80
EXPOSE 80