---
title: Guides - Database Configuration
version: head
---

# Database Configuration

Before starting your server, you need to configure the database link in <code>.env*</code> files.

Open this file for each environment and update <code>DATABASE_URL</code> for your database.

## <a href="http://www.postgresql.org/" target="_blank">PostgreSQL</a>

Setup database variable for the development environment:

```
# .env.development
DATABASE_URL="postgresql://username:password@localhost/bookshelf_development"
```

Setup database variable for the test environment:

```
# .env.test
DATABASE_URL="postgresql://username:password@localhost/bookshelf_test"
```

# Setup your database

After your database variables setup is done you need to create the database and run the migrations before being able to launch a development server.

In your terminal, enter:

```
% bundle exec hanami db prepare
```

To setup your test environment database, enter:

```
% HANAMI_ENV=test bundle exec hanami db prepare
```
