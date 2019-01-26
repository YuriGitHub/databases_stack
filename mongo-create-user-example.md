# Mongo Settings

### User  for specific database
```js

use identyhub_shared_user-test

db.createUser(
   {
     user: "mongo-shared-user-test",
     pwd: "mongo-shared-pass",
     roles: [ { role: "readWrite", db: "identyhub_shared_user-test" },
             { role: "read", db: "identyhub_shared_user-test" },
             { role: "dbAdmin", db: "identyhub_shared_user-test" } ]
   }
);


use identyhub_shared_user-dev

db.createUser(
   {
     user: "mongo-shared-user-dev",
     pwd: "mongo-shared-pass",
     roles: [ { role: "readWrite", db: "identyhub_shared_user-dev" },
             { role: "read", db: "identyhub_shared_user-dev" },
             { role: "dbAdmin", db: "identyhub_shared_user-dev" } ]
   }
);



```
