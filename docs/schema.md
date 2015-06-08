# Schema Information

## users
column name    | data type | details
---------------|-----------|--------
id             | integer   | not null, primary key
email          | string    | not null
session_token  | string    | not null, unique
password_digest| string    | not null
fname          | string    | not null
lname          | string    | not null

## books
column name | data type | details
------------|-----------|--------
id          | integer   | not null, primary key
title       | string    | not null
release_date| date      | not null
author_id   | integer   | not null, foreign key
doc_url     | string    | not null

## reviews
column name | data type | details
------------|-----------|--------
id          | integer   | not null, primary key
author_id   | integer   | not null, foreign key
book_id     | integer   | not null, foreign key
quantitative| integer   | not null
qualitative | text      |

## library-items
column name | data type | details
------------|-----------|--------
id          | integer   | not null, primary key
book_id     | integer   | not null, foreign key
owner_id    | integer   | not null, foreign key

## subjects
column name | data type | details
------------|-----------|--------
id          | integer   | not null, primary key
title       | string    | not null

## book-subjects
column name | data type | details
------------|-----------|--------
id          | integer   | not null, primary key
book_id     | integer   | not null, foreign key
subject_id  | integer   | not null, foreign key

## collections
column name | data type | details
------------|-----------|--------
id          | integer   | not null, primary key
title       | string    | not null
description | string    |
creator_id  | integer   | not null, foreign key

## collection-books
column name  | data type | details
-------------|-----------|--------
id           | integer   | not null, primary key
book_id      | integer   | not null, foreign key
collection_id| integer   | not null, foreign key

## collection-comments
column name  | data type | details
-------------|-----------|--------
id           | integer   | not null, primary key
author_id    | integer   | not null, foreign key
content      | string    | not null
collection_id| integer   | not null, foreign key

## followed-collections
column name  | data type | details
-------------|-----------|--------
id           | integer   | not null,
follower_id  | integer   | not null, foreign key
collection_id| integer   | not null, foreign key
