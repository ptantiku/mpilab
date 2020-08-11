# MPI Alpine on Single-Host Cluster

*This work is based on Alpine MPICH by Nguyen Nguyen (NLKNguyen) at https://github.com/NLKNguyen/alpine-mpich.*

This code is for setting up a cluster of MPICH Alpine container on a single host, for purpose of teaching parallel labs.

## Get started

- **setup cluster**: Just run `docker-compose up -d --scale worker=3` or simply `./cluster.sh up size=4`
- **login**: To login into master node, run `./cluster.sh login`
- **source file(s)**: source file(s) can be placed into ./project folder which will be mounted into /project in the containers. To modify this configuration, edit docker-compose.yaml under "volumes".
- **compile**: Use `mpicc` to compile, e.g. `mpicc -o hellworld helloworld.c`
- **run**: Use `mpirun`, e.g. `mpirun -n 4 ./helloworld`
- **exit**: Type `exit`

