## Install PostSQL for python library

The query execution is based on PostgreSQL's python library -- [PyGreSQL](http://www.pygresql.org/), it needs to be installed on the server first.
1. On terminal, open bash
```
  $sudo bash
```
2. Adding system variables
```
  $export CFLAGS=-Qunused-arguments
  $export CPPFLAGS=-Qunused-arguments
```
3. Install using pip:
```
  $pip install PyGreSQL
```

## Set up:
1. Clone this repo
2. Config your database name, host, port, user name, and password in ```connection.py```
```python
db = DB(dbname='',host='',port= ,user='',passwd='')
```
3. Deploy this to server
4. Add this integration to your Slack
5. All set!

## Slack command:
- create table:
```
  /sql create table users(id primary key, name varchar)
```
- Insert data:
```
  /sql insert into users values(1, 'Seth Wang')
```
- selection:
```
  /sql select users.name from users where id=1
```
- deletion
```
  /sql delete from users where id=2
```