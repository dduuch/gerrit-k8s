### Initialize Gerrit

Run the Gerrit image manually to initialize the Gerrit directories. Paths vary by machine.

```
docker run -it \
-v ~/.docker/Volumes/gerrit-db-claim/pvc-1e116a19-0e9c-11e8-aa5f-025000000001/:/var/gerrit/db/ \
-v ~/.docker/Volumes/gerrit-index-claim/pvc-1e1afa26-0e9c-11e8-aa5f-025000000001/:/var/gerrit/index/ \
-v ~/.docker/Volumes/gerrit-cache-claim/pvc-1e15c2f2-0e9c-11e8-aa5f-025000000001/:/var/gerrit/cache/ \
-v ~/.docker/Volumes/gerrit-cache-claim/pvc-1e15c2f2-0e9c-11e8-aa5f-025000000001/:/var/gerrit/git/ \
 gerritcodereview/gerrit:latest '/usr/bin/java -jar /var/gerrit/bin/gerrit.war init -d /var/gerrit/'
```
