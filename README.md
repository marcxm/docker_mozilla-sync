# docker_mozilla-sync

Customized, yet official mozilla sync server. Still uses Mozilla account, BUT it's only for authentication [like LDAP/AD].
The data itself resides in sqlite3 database in ./syncserver/syncserver.db.

1. modify docker-compose.yml as required
2. in Firefox, go to URL bar, enter "about:config", search for "identity.sync.tokenserver.uri" and change it to your server address [DNS+port]:

identity.sync.tokenserver.uri:  http://my.domain:5000/token/1.0/sync/1.5