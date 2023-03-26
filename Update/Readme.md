**First you must be in cd home folder:** 
```pthon
cd ~
```
**Then backup your node:**
```python
docker cp muon-node:/usr/src/muon-node-js/.env ./backup.env
```
**Then remove old node:**
```python
docker stop muon-node redis mongo 
docker rm muon-node redis mongo 
rm muon-node-js -rf
```
**Then install new node:**
```python
curl -o docker-compose.yml https://raw.githubusercontent.com/muon-protocol/muon-node-js/testnet/docker-compose-pull.yml
docker-compose pull
docker-compose up -d
```
**Then restore the backup:**
```python
docker cp backup.env muon-node:/usr/src/muon-node-js/backup.env
docker exec -it muon-node ./node_modules/.bin/ts-node ./src/cmd keys restore backup.env
docker restart muon-node
```

**By following these steps, your node will be upgraded, and you can continue contributing to the network without any issues. We highly appreciate your prompt action on this matter, as it helps maintain the stability and performance of our network.
Thank you for your continued support and cooperation. If you have any questions or concerns regarding this update, please do not hesitate to reach out to our support team.**
