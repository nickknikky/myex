[Home](../)
1. To add environment variables

	i. Create a file with a _.sh_ extension inside /etc/profile.d/ and add commands to it. You will need to re-login to enable these.

	[Cf. https://stackoverflow.com/a/35357011/6670698](https://stackoverflow.com/a/35357011/6670698)


2. To install PHP 7 and other packages that are reported as:
	ERROR: unsatisfiable constraints:
  		&lt;package-name&gt; (missing):
    		required by: world[&lt;package-name&gt;]

		apk add --update --repository http://dl-cdn.alpinelinux.org/alpine/edge/main --repository http://dl-cdn.alpinelinux.org/alpine/edge/community

	[Cf. https://stackoverflow.com/a/39921218/6670698](https://stackoverflow.com/a/39921218/6670698)

3. If Step 2. does not work for you then

	i. edit your file /etc/apk/repositories and uncomment the lines that look like the following:

		http://xxx.yyy.zzz/alpine-linux/edge/main
		http://xxx.yyy.zzz/alpine-linux/edge/community

	ii. save and exit and run the following:

		apk update

	iii. Verify using

		apk info php7

	[Cf. https://wiki.alpinelinux.org/wiki/Alpine_Linux_package_management](https://wiki.alpinelinux.org/wiki/Alpine_Linux_package_management)
