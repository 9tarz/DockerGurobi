# DockerGurobi

[How to install docker](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04)

## Build an image
```console
$ git clone https://github.com/9tarz/DockerGurobi.git
$ cd DockerGurobi
$ sudo docker build -t my-gurobi-app .
```

## Run the code
Assume you already have WLS client license file (gurobi.lic) in  ```$PWD/gurobi.lic ```
```console
$ echo $PWD
/home/kanatip/
$ ls $PWD
PolynomialObliviousRouting  gurobi.lic
$ sudo docker run --volume=$PWD/gurobi.lic:/opt/gurobi/gurobi.lic:ro --volume=$PWD/PolynomialObliviousRouting:/app my-gurobi-app
```
