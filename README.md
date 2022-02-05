# Server Command

## scp

* file

~~~
scp -P [port number] [local path] [username]@[server ip]:[destination path]
~~~

* if Permission denied you may check owner and group of destination forder
  and change the owner or group with next code

  * change user 
  ~~~
  sudo chown [username] [destination forder]
  ~~~

  * change group
  ~~~
  sudo chgrp -R [destination forder]
  ~~~

* and you may also change permission. to write this code, you have to login to server using ssh 
  ~~~
  chmod 777 [destination forder path]
  ~~~

example
~~~
sudo chown aailab mjkim
~~~
change the user of mjkim forder to aailab

~~~
sudo chgrp -R aailab mjkim
~~~
change the group of mjkim forder to aailab

~~~
ssh [username]@[ip] -p [port number]
chmod 777 ./mjkim
~~~
change the permission to read, write, execute

then you can use scp command
~~~
logout
scp -r -P [port number] [local path] [username]@[ip]:[destination path]
~~~
