use identyhub_shared_user
db.createUser(
   {
     user: "mongo-shared-user",
     pwd: "mongo-shared-pass",
     roles: [ { role: "readWrite", db: "identyhub_shared_user" },
             { role: "read", db: "identyhub_shared_user" },
             { role: "dbAdmin", db: "identyhub_shared_user" } ]
   }
);
