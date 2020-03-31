
# BigData
|Subject name| Year |
|--|--|
| Podstawy przetwarzania dużych zbiorów danych  | 2019/2020 |

Projects from this repository are ment to be run in *cloudera* environement.
## Compilation
In order to compile desired project:

 - navigete into project directory i.e.: `cd Week3/ImageCounter`
 - create a fat jar with maven: `mvn clean package`
 - transfer compiled jar file into binded directory
 - run jar file from cloudera environement: `hadoop jar BigData-1.0-SNAPSHOT.jar solution.ImageCounter log_INPUT log_OUTPUT`

## Cloudera environement
In order to run *cloudera/quickstart* docker container with a binded catalogue (**please change source direcory** - '*/home/kjawo/cloudera*' ) execute:
```bash
docker run --hostname=quickstart.cloudera --mount type=bind,source="/home/kjawo/cloudera",target=/mnt/shared --privileged=true -t -i -p 8888  
:8888 -p 7180:7180 cloudera/quickstart /usr/bin/docker-quickstart
```

or create an alias:

```bash
alias clouderad='docker run --hostname=quickstart.cloudera --mount type=bind,source="/home/kjawo/cloudera",target=/mnt/shared --privileged=true -t -i -p 8888  
:8888 -p 7180:7180 cloudera/quickstart /usr/bin/docker-quickstart'
```
