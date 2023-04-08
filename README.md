# Boilerplate for nginx with Let’s Encrypt on docker-compose 

`init-letsencrypt.sh` fetches and ensures the renewal of a Let’s
Encrypt certificate for one or multiple domains in a docker-compose
setup with nginx. Unlike https://github.com/wmnnd/nginx-certbot, this repo
uses Route53 DNS challenge. 

## Installation
1. [Install docker-compose](https://docs.docker.com/compose/install/#install-compose).

2. Clone this repository: `git clone https://github.com/clemthom/certbot-route53.git`

3. Modify configuration:
- Add domains and email addresses to init-letsencrypt.sh
- set the AWS access key and secret key in `.env` More info about this in https://certbot-dns-route53.readthedocs.io/en/stable/
4. Run the init script:

        ./init-letsencrypt.sh

5. Run the server: (if you require renewal to be taken care too)

        docker-compose up

## License
All code in this repository is licensed under the terms of the `MIT License`. For further information please refer to the `LICENSE` file.
