# nodejs command line cheatsheet


### Kill a node processing using a particular port
--------------------------------------------------
1. List all processes that are using the TCP ports

  Mac: `sudo lsof -i -n -P | grep TCP`

  Linux: `netstat -tulpn`

2. Find the process id (PID) of the node process and then run:

  `kill -9 PID`


### Start server in production mode
----------------------------------
- Use forever
  ```
  NODE_ENV=production forever start server.js
  ```

- Use forever and nodemon

  ```
  NODE_ENV=production forever start --killSignal=SIGTERM -c nodemon server.js
  ```

- Use tmux

  ```
  NODE_ENV=production node server.js
  ```

- Use tmux and nodemon

  ```
  NODE_ENV=production nodemon server.js
  ```
