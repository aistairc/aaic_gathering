#!/bin/bash

#PBS --group=g-nairobi
#PBS -q gq
#PBS -b 2
#PBS -l cpunum_job=40
#PBS -l gpunum_job=8
#PBS -l elapstim_req=00:05:00
#PBS -T openmpi
#PBS -v NQSII_OMPI_MODVER=1.10.4/gcc4.8.5_cuda8.0
#PBS -N chainermn-test

cd ${PBS_O_WORKDIR}
SINGULARITY_CONTAINER=aaic-base-gpu.img
mpirun -x PATH -n 16 ${NQSII_MPIOPTS} --npersocket 4 singularity exec --nv ${SINGULARITY_CONTAINER} python chainermn-1.0.0b2/examples/mnist/train_mnist.py --epoch 20 --batchsize 100 -g
