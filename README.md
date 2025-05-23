# RTOS-Final-Project
This is our Final Project Repository for ENPM818J

Authored by:
- Zachary Steinberg
- Troy Bates

## Final Project Presentation

Here is our final presentation: [Final Presentation Link](https://docs.google.com/presentation/d/1q5KIJI5jbNL6v5L2D7ayR7ZGshla-eqgIjCNhvCPU5o/edit?usp=sharing)

## Project Requirements

1. Integrate cFS with FreeRTOS on the Pi Pico 
2. Implement or adapt the OSAL (Operating System Abstraction Layer) for the Pi Pico 
3. (OSAL Sub Rq) The system will allow the create and manage multiple concurrent tasks 
4. (OSAL Sub Rq) The system shall support inter-task synchronization (mutexes, semaphores, or message queues) 
5. (OSAL Sub Rq) The system shall implement sleep functions 
6. Port PSP to run on the Pi Pico 
7. (PSP Sub Rq) The system shall use the PSP in order to initialize all required hardware components before cFS startup. Including but not limited to system clock, on board memory, and applicable peripherals 
8. (PSP Sub Rq) The system shall enable through the PSP a software system reset 
9. Run basic cFS application (Hello World esk) to demonstrate system capabilities 
10. Create instructions and Documentation for how to run cFS with OSAL and PSP modules implemented with freeRTOS on the Pi Pico 

## In this repo

### freeRTOS_ports 

This directory has the freeRTOS ports that we added to the cFS freeRTOS library. We were able to fully implement the RP2040 port with OSAL and get the project built. We were not able to compile OSAL due to the memory limitations of the Pi Pico board.

### RP2040_freeRTOS_demo

This demo was taken from the [freeRTOS SMP Demos](https://www.freertos.org/Documentation/02-Kernel/02-Kernel-features/13-Symmetric-multiprocessing-introduction). We modified the blinky demo by adding print statements to visualize and log the freeRTOS tasks. We ran this demo to validate that the RP2040 freeRTOS port was working properly before integrating it into our OSAL project.

## cFS Fork

Here is the fork of the cFS-freeRTOS repo that we made from pztrick's fork: [cFS Fork](https://github.com/zstein13/cfs-freertos/tree/main)

Our repo has two development branches that were never merged to main:

- zs
- tbates-dev

These branches have our configurations that we made to get the cFS container built on our machines.

## OSAL Fork

Here is the OSAL fork that we made from pztrick's fork: [OSAL Fork](https://github.com/too9le/osal)

Our repo has two development branches that were never merged to main:

- zstein-dev
- tbates-dev

Most of our work was in the tbates-dev branch. We created two branches initially because the two of us were working in parallel to get OSAL running.

