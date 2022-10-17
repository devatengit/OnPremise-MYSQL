# OnPremise-MYSQL

If you want to run On-Premise Dashboard and On-Premise MySQL Agent Separately, for that we are providing [On-Premise Dashboard](https://github.com/devatengit/Devaten-OnPremise-Dashboard) and [OnPremise MySQL](https://github.com/devatengit/OnPremise-MYSQL) Agent files separately.

For that run [On-Premise Dashboard](https://github.com/devatengit/Devaten-OnPremise-Dashboard). Once its up and runnig minimize the Command Prompt. 

Now open On-Premise MySQL Docker Compose file. In ```environment:``` there is an ActiveMQ URL to conncet On-Premise Dashboard. In URL replace the ```127.0.0.1```:61616 with your systems IP Address. 

- spring.activemq.broker-url=tcp://```IP_ADDRESS```:61616

Once the change is done ```save``` the file. 

Open cmd at that location where docker-compose.yml exists and run the following commands:
```
docker compose pull
```
to pull image locally
```
docker compose up
```
to run the image/container exist in docker compose file.

Once it run successfully you'll get ``` Agent Unique ID ``` which is useful when you are going to add ```Agent```.

