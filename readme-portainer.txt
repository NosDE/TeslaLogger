1: git clone https://github.com/NosDE/TeslaLogger.git
2: cd TeslaLogger
3: mkdir GrafanaDashboards
4: docker-compose build

5: Open Portainer, go to “Stacks” and select “Add stack”
Give it a name, e.g. “teslalogger” and select “Git repository” as build method
	Repository URL: https://github.com/NosDE/TeslaLogger/
	Repository reference: refs/heads/master
	Compose path: docker-compose.portainer.yml

Add environment variables as follows in “advanced mode”:

TESLALOGGER_DIR=/root/docker/TeslaLogger
MYSQL_USER=teslalogger
MYSQL_PASSWORD=teslalogger
MYSQL_DATABASE=teslalogger
MYSQL_ROOT_PASSWORD=teslalogger
GRAFANA_PASSWORD=teslalogger

Hit “Deploy the stack”, wait for 5-10 minutes and then go to http://<your host>:8888/admin. 
