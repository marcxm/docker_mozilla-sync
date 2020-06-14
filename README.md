# docker_mozilla-sync

Customized, yet official mozilla sync server. Still uses Mozilla account, BUT it's only for authentication [like LDAP/AD].
The data itself resides in sqlite3 database in ./syncserver/syncserver.db.

1. modify docker-compose.yml as required
2. in Firefox, go to URL bar, enter "about:config", search for "identity.sync.tokenserver.uri" and change it to your server address [DNS+port]:

identity.sync.tokenserver.uri:  http://my.domain:5000/token/1.0/sync/1.5

3. once ./syncserver/syncserver.db is created make sure that whole directory and a file belongs to user / group: 1001 / 1001:

chown -R 1001:1001 syncserver

+ to make sure [if file access time does not change after a sync]:

chmod 777 syncserver/syncserver.db

