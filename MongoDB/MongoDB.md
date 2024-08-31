# MongoDB

MongoDB.md

https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/

```

cat /etc/lsb-release

sudo apt-get install gnupg curl

curl -fsSL https://www.mongodb.org/static/pgp/server-7.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg \
   --dearmor

echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list

sudo apt-get update

sudo apt-get install -y mongodb-org

echo "mongodb-org hold" | sudo dpkg --set-selections
echo "mongodb-org-database hold" | sudo dpkg --set-selections
echo "mongodb-org-server hold" | sudo dpkg --set-selections
echo "mongodb-mongosh hold" | sudo dpkg --set-selections
echo "mongodb-org-mongos hold" | sudo dpkg --set-selections
echo "mongodb-org-tools hold" | sudo dpkg --set-selections

```

```
# The data directory 

## /var/lib/mongodb

ls /var/lib/mongodb

# The data directory 

## /var/lib/mongodb

ls /var/lib/mongodb

## configuration file (/etc/mongod.conf).

cat /etc/mongod.conf

```

```
## 
ps --no-headers -o comm 1

```
```
# Start MongoDB.

sudo systemctl start mongod
sudo systemctl daemon-reload
sudo systemctl status mongod
sudo systemctl enable mongod
sudo systemctl stop mongod
sudo systemctl restart mongod

```

```
mongosh
Current Mongosh Log ID: 66d351451f35111f1e5e739b
Connecting to:          mongodb://127.0.0.1:27017/?directConnection=true&serverSelectionTimeoutMS=2000&appName=mongosh+2.3.0
MongoNetworkError: connect ECONNREFUSED 127.0.0.1:27017

```
