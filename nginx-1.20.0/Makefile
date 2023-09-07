
default:	build

clean:
	rm -rf Makefile objs

.PHONY:	default clean

build:
	$(MAKE) -f objs/Makefile

install:
	$(MAKE) -f objs/Makefile install

modules:
	$(MAKE) -f objs/Makefile modules

upgrade:
	/home/sallen/linux/nginxtools/nginx-1.20.0/install/sbin/nginx -t

	kill -USR2 `cat /home/sallen/linux/nginxtools/nginx-1.20.0/install/logs/nginx.pid`
	sleep 1
	test -f /home/sallen/linux/nginxtools/nginx-1.20.0/install/logs/nginx.pid.oldbin

	kill -QUIT `cat /home/sallen/linux/nginxtools/nginx-1.20.0/install/logs/nginx.pid.oldbin`

.PHONY:	build install modules upgrade
