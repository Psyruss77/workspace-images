FROM gitpod/workspace-full

# Install MongoDB
# Source: https://www.digitalocean.com/community/tutorials/how-to-install-mongodb-on-ubuntu-20-04
RUN curl -fsSL https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add - && \
    echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list && \
    sudo apt-get update && \
    sudo apt-get install -y mongodb-org && \
    sudo rm -rf /var/lib/apt/lists/* && \
    sudo mkdir -p /data/db && \
    sudo chown gitpod:gitpod -R /data/db
