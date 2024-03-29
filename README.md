# Quick reference

-	**Maintained by**: [PilotFish Technology, LLC](https://www.pilotfishtechnology.com)

-	**Where to get help**: [PilotFish Technology CMS](https://cms.pilotfishtechnology.com)

-   **Docker Images**: [Docker Hub](https://hub.docker.com/u/pilotfishtechnology)

-   **Source**: [GitHub](https://github.com/pilotfishtechnology)

# What is eiPlatform?
The eiPlatform enterprise integration solution is a complete Java framework that leverages application server technology, web services and industry XML standards to enable the deployment of internal and external system interfaces better, faster and less expensively than ever before possible. When combined with the graphical IDE component, the eiConsole, the developer has the most comprehensive solution for enterprise integration.

[www.pilotfishtechnology.com/enterprise-integration-platform/](https://www.pilotfishtechnology.com/enterprise-integration-platform/)

![logo](https://www.pilotfishtechnology.com/wp-content/uploads/2015/03/pilotfish-logo.png)

## Using `docker-compose` (Recommended)

1. Install Docker

	- [Docker Install documentation](https://docs.docker.com/install/)
	- [Docker-Compose Install documentation](https://docs.docker.com/compose/install/)

2. Clone the main branch of the [repository](https://github.com/pilotfishtechnology/eiplatform_docker_compose_example)

	```bash
	cd /opt
	git clone https://github.com/pilotfishtechnology/eiplatform_docker_compose_example
	cd eiplatform_docker_compose_example
	```

3. Log in to the [Customer Portal](https://customerportal.pilotfishtechnology.com/portal/login.html) and download your latest license file.

4. Convert your license file to a base64 encoded string (`echo "$(cat pflicense.key | base64)"`) and copy the base64 encoded string into the `PFISH_EIP_CONF_com_pilotfish_eip_license_base64` environment variable located in the docker-compose.yml

5. Bring up your stack by running

	```bash
	docker-compose up -d
	```

When your docker container is running, connect to it on port `8080` to access the eiplatform instance.

[http://127.0.0.1:8080/eip/](http://127.0.0.1:8080/eip/)
