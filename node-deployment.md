# Nodejs Deployment by pm2
 # Pm2

### Pm2 is a node process manager for Nodejs application. It allows you to manage, monitor, and deploy Node.js applications as background processes or daemons, making it easier to ensure that your Node.js applications run reliably in production environments.

**Node version install**
   
       # npm install v0.0.0

**Use the node version which is required**

       # nvm use v0.0.0

**Installs a package and any packages that it depends on.**

       # npm install

**Creates a build directory with a production build of your app.**
             
       # npm run build 

**Install pm2 with npm**

       # npm install pm2 -g

**PM2 module to automatically rotate logs of processes managed by PM2.**
 
       # pm2 install pm2-logrotate

**Let's start pm2 with file**

       # pm2 start config.js

**Lists all running applications managed by pm2.**

       # pm2 ls/list

**This command is used to save the currently running processes managed by pm2 as a configuration file**

       # pm2 save

**Displays logs for a specific application.**

       # pm2 logs id/file name

**Restarts a specific application.**

       # pm2 restart id/file name