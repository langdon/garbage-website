# Use the Fedora Minimal base image
FROM registry.access.redhat.com/ubi8-minimal

# Install Apache httpd
RUN microdnf -y install httpd && microdnf clean all

# Copy the HTML file
COPY index.html /var/www/html/

# Use httpd as the entrypoint, and run it in the foreground
CMD [ "/usr/sbin/httpd", "-D", "FOREGROUND" ]
