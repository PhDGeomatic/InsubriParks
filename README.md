
<div>

<img 
  src="https://github.com/PhDGeomatic/InsubriParks/blob/main/uploads/logoInsubriParks.png"
  alt="logo"
/>

# InsubriParks Dashboard

</div>

Dashboard to administrate geodata collected with the Telegram bot ["Geo Collector Bot"](https://github.com/opengeolab/geocollectorbot).  
This web application is developed within the project [INSUBRI.PARKS](https://insubriparksturismo.eu) funded by the Interreg Co-operation Programme Italy–Switzerland 2014 -2020 (ID 605472).

## Documentation

To know how the Dashboard works you can follow the documentation:
* [overview](./docs/10_overview.md)
* [usage](./docs/20_usage.md)
* [configuration](./docs/30_configuration.md)

## Enable SSL

On the machine, run

```shell
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ./nginx/ssl/nginx-selfsigned.key -out ./nginx/ssl/nginx-selfsigned.crt
sudo openssl dhparam -out ./nginx/ssl/dhparam.pem 4096
```

### Resources

- https://mpolinowski.github.io/docs/DevOps/NGINX/2020-08-27--nginx-docker-ssl-certs-self-signed/2020-08-27/
- https://www.digitalocean.com/community/tutorials/how-to-create-a-self-signed-ssl-certificate-for-nginx-in-ubuntu-22-04
- https://codingwithmanny.medium.com/configure-self-signed-ssl-for-nginx-docker-from-a-scratch-7c2bcd5478c6

## Contributions

[GEOlab](http://www.geolab.polimi.it/) - Politecnico di Milano (contact: [Daniele Oxoli](mailto:daniele.oxoli@polimi.it))

Developed by G.Z. - GeoDev@[PhDGeomatic](https://github.com/PhDGeomatic)

## License

[MIT](https://opensource.org/licenses/MIT) © [GEOlab](mailto:geolab.como@gmail.com)
