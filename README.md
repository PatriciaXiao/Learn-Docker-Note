# Learn-Docker-Note
 My Note learning docker as a beginner

## Motivation
- To running with my own environmental settings on Github without root permission (and I actually don't think I should have it, root is evil for a beginner like me)
- To not setting the environment again and again from place to place; I want something that could quickly get it run anywhere.

## Tools
- On our lab's server (Scai1) the Docker is already well-installed
- For learning purpose I also [installed Docker-Desktop on my local mac](https://docs.docker.com/docker-for-mac/install/)

## Tutorials
- [official tutorial upon installing](https://hub.docker.com/?overlay=onboarding)
    * official example contained [here](https://github.com/docker/doodle), I put the examples and the readme in [./official-examples/](./official-examples/)
        * I tried:
            ```shell
            cd cheers2019
            docker build -t patriciaxiao/cheers2019 .
            ```
            where *patriciaxiao* is my Docker username, as is registered with Docker, on its official website upon downloading. 
            Then:
            ```shell
            docker run -it --rm patriciaxiao/cheers2019
            ```
        * In order to share it *with the world* I could:
            ```shell
            docker login
            docker push patriciaxiao/cheers2019
            ```
        * In order to use it, from another place we say:
            ```shell
            docker pull patriciaxiao/cheers2019
            ```
            and then
            ```shell
            ocker run -it --rm patriciaxiao/cheers2019
            ```
        * my repositories will be managable [here online](https://hub.docker.com/r/patriciaxiao/)
        * to stop all containers we use:
            ```shell
            docker container stop
            ```
- [official documentation](https://docs.docker.com/)

## Starter Commands
* To run Ubuntu environment:
    ```docker run -i -t ubuntu /bin/bash ```
    and exit by CTRL+P+Q

## Flags Cheatsheet ([reference](https://docs.docker.com/engine/reference/run/))
| flag      | explanations                                                                             |
| :-------: | :--------------------------------------------------------------------------------------: |
| ```-it``` | interactive; somewhat equivalent with ```-i -t```, but ```-t``` usage is more restricted |


