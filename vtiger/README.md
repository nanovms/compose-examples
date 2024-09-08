This is a compose example for running a vtiger crm unikernel talking to a
mysql unikernel.

Note: This is really only for local dev work - you'll want to front-end
or host your vtiger pkg differently for prod.

```
ops compose up
```

First login to your mysql and create the database.

```
create database vtiger;
grant all on vtiger.* to vtiger@'%' identified by 'vtiger';
flush privileges;
alter database vtiger character set utf8 collate utf8_general_ci;
```

Then you can login to vtigercrm and finish the install.
