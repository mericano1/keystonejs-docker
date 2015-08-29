# KeystoneJS Dockerized

[mahnunchik/keystonejs](https://registry.hub.docker.com/u/mahnunchik/keystonejs/) is a [docker](https://docker.com) image of [KeystoneJS](http://keystonejs.com) cms.

[KeystoneJS](http://keystonejs.com) is a powerful new Node.js content management system and web app framework built on [express](http://expressjs.com) and [mongoose](http://mongoosejs.com) that makes it easy to create sophisticated web sites and apps, and gives you a beautiful, auto-generated Admin UI.

Official GitHub repository: [JedWatson/keystone](https://github.com/JedWatson/keystone)

## Usage

Run MongoDB as separate container:

	docker run -d --name mongo mongo

Run KeystoneJS linked with MongoDB:

	docker run --rm -p 8080:8080 --link mongo:mongo --entrypoint /bin/bash mahnunchik/keystonejs -c "export CLOUDINARY_URL=cloudinary://<signup for a url>; export MONGO_URI=mongodb://mongo:27017/; node keystone.js"
