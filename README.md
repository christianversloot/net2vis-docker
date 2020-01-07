# net2vis-docker

For academic and other publications, it's quite difficult to create neural network visualizations that are sparse yet make sense. Tools that are available often produce _vertical_ visualizations rather than horizontal ones. Fortunately, there is a solution:

[Net2Vis](https://github.com/viscom-ulm/Net2Vis)

It's a React based web application that generates neural network visualizations for Keras models and was created by [Bäuerle & Ropinski (2019)](https://arxiv.org/abs/1902.04394).

Installing Net2Vis is however quite difficult as various dependencies are required, such as Cairo, especially on Windows. To avoid this trouble, I created a Docker configuration which allows you to run both Net2Vis frontend and backend on a Windows machine with only one command, yet access Net2Vis from the browser on your host machine - just as you'll do when running Net2Vis on your host OS.

## How to use net2vis-docker

1. Install Docker:
    - https://docs.docker.com/install/
2. Install Docker Compose:
    - https://docs.docker.com/compose/install/
3. Clone this repository:
    - `git clone https://github.com/christianversloot/net2vis-docker.git`
4. Run it from the folder:
    - `docker-compose up` (run in front)
    - `docker-compose up -d` (run in the background)
5. Access from http://localhost:3000/

The first time, it will likely take some time to start the Docker containers, as the containers need to be built (installing the Net2Vis repository and dependencies takes some time). Every other time, startup should go quite fast.

## Original work
Bäuerle, A., & Ropinski, T. (2019). [Net2Vis: Transforming Deep Convolutional Networks into Publication-Ready Visualizations](https://arxiv.org/abs/1902.04394). arXiv preprint arXiv:1902.04394.

https://github.com/viscom-ulm/Net2Vis

## License
The licenseable parts of this code are licensed under the [MIT License](./LICENSE).

## Read more?
MachineCurve. (2020, January 7). Visualizing Keras neural networks with Net2Vis and Docker. Retrieved from https://www.machinecurve.com/index.php/2020/01/07/visualizing-keras-neural-networks-with-net2vis-and-docker/