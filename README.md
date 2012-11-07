postgres-commands
=================

My postgres learning 

Create Database
===

create database hgtv;

Grant Access to database hgtv for user sqlalchemy
====

grant all privileges on database hgtv to sqlalchemy;

Add Column
==========

ALTER TABLE proposal add user_id integer not null;

Remove Constraint
=========

alter table proposal remove constraint fk_user_id foreign key (id) references "user"(id) match full; 

Alter column
=====

ALTER TABLE proposal ALTER is_speaking TYPE int USING CASE WHEN is_speaking=FALSE THEN 0 ELSE 1 END;

Add FK constraint
======
alter table proposal add constraint fk_user_id foreign key (user_id) references "user"(id) match full; 

Display table schema
====
\d tablename