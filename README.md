- [x] created git repo
- [x] created hello world flask app
- [x] installed NGINX with homebrew (for mac system)
- [ ] configure NGINX


TODO: go through at each step create a branch that can be checked out with instructions on each


description
===========
Give a short description of what NGINX and of what uWSGI are.


install section
===============
- NGINX
- uWSGI
- python
- flask


show explicitly where important nginx files are after install
on ubuntu, on mac, etc

remind readers to set the log destinations for both nginx and uwsgi

you can set the log directories to be anywhere, even in your project folder, but most people find it useful to save them in a directory called /var/log. so make /var/log/nginx/ and /var/log/uswgi.
(remind readers to check up on the logs later if something goes wrong)

for a web app to be hosted on the internet, nginx will have to run the server for the website, and uwsgi will have to be running the application on that server.

the nginx command to start the server is just `nginx`, and `nginx -s reload` to reload. When nginx loads, it needs to check your settings in the "nginx.conf" configuration file located at usr/local/nginx/nginx.conf. you can see in the configuration file, nginx.conf `includes` other files (all of the files in server/ on a mac configuration, and all of the \*.conf files in the usr/local/nginx folder on an ubuntu configuration) we recommend creating a file called something.conf that is included and read by the nginx.conf when the server starts up.

to start uWSGI with custom configuration, we will use the `uswgi --ini <file>` command. This way we can specify the configuration file to use for this session. This is how to make the file :

`filename.ini`

```ini
asdf;hdasg
fdsa;k;dgsa
asghkjg```


okay now that that's done, lets do it
the end
