# DockerGurobi

## How to use it
Assume you already have WLS client license file (gurobi.lic) in  $PWD/gurobi.lic
```console
$ git clone https://github.com/9tarz/DockerGurobi.git
$ cd DockerGurobi
$ docker build -t my-gurobi-app .
$ sudo docker run --volume=$PWD/gurobi.lic:/opt/gurobi/gurobi.lic:ro --volume=$PWD/PolynomialObliviousRouting:/app my-gurobi-app
```
