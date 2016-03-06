# docker-simplesamlphp

SimpleSAMLphp docker image based on Debian + Apache + mod_ssl

This image is not intended for production use. It is only suitable for testing and lab environments. Please be aware of this.

You can use this image just by typing:

docker run -d -p 8080:80 -p 8443:443 -v /path/to/config:/var/simplesamlphp/config -v /path/to/metadata:/var/simplesamlphp/metadata edelahozuah/simplesamlphp

Then, access SSP:
https://localhost:8443:/simplesaml/

This may not work in Mac OS X. In that case, you have to use docker-machine IP address for the host part of the URL. You can get that IP by typing:

docker-machine ip

Let's say it is 192.168.99.100. Then, you should access your container by typing:

https://192.168.99.100:8443/simplesaml/

Apache configuration is embedded into the image. You can set any configuration that you want in ./etc/apache2/sites-enabled/

Also, you can find a binary version of this image at docker hub: 

https://hub.docker.com/r/edelahozuah/simplesamlphp/


