# beehive-survey
Tryin out  https://github.com/muesli/beehive/


## Install & run

```bash
# export URI_REPO_BEEHIVE=https://github.com/Jean-Baptiste-Lasselle/beehivey
export URI_REPO_BEEHIVE=https://github.com/muesli/beehive

rm -rf beehivey
cd beehivey
git clone $URI_REPO_BEEHIVE .
cd docker
# docker build -t beehive .
docker build -t poste-devops-typique:5000/pegasus-devops-io/beehive:0.0.1 .
# docker push poste-devops-typique:5000/pegasus-devops-io/beehive:0.0.1 .

# Running Beehive
# docker run -d -p 8181:8181 -v beehivey:/conf/:rw gabrielalacchi/beehive
docker run -itd -p 8181:8181 -v beehivey:/conf/:rw gabrielalacchi/beehive
```

```bash
rm -rf beehivey
cd beehivey
docker pull gabrielalacchi/beehive
# docker run --name beehive -d -p 8181:8181 gabrielalacchi/beehive
docker run -d -p 8181:8181 -v beehivey:/conf/:rw gabrielalacchi/beehive
```

Then I get something at :  http://poste-devops-typique:8181/admin 

Note that `poste-devops-typique` is a host name for a simple VM created on my workstation, on which I installed docker-compose.yml, and a private docker registry at `poste-devops-typique:5000`, just a pure basis one `registry:2` based.

