# Git

`docker build . -t git`

you need to mount the `/output` to access files like in

`
docker run  -v ${PWD}:/output git clone https://github.com/jeanlaurent/redirect-custom-handler.git
`

If you need to clone private repository you have to mount your `~/.ssh`

`
docker run -v ${PWD}:/output -v ${HOME}/.ssh/:/root/.ssh git clone git@github.com:jeanlaurent/redirect-custom-handler.git
`
