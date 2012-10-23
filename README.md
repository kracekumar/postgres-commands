postgres-commands
=================

My postgres learning 

Add Column
==========

ALTER TABLE proposal add user_id integer not null;

Remove Constraint
=========

alter table proposal remove constraint fk_user_id foreign key (id) references "user"(id) match full; 

Add FK constraint
======
alter table proposal add constraint fk_user_id foreign key (user_id) references "user"(id) match full; 

Display table schema
====
\d tablename