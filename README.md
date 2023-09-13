# Side Projects

This repository contains a list of side projects I have worked on and plan to work on broken down by domain. Although each project should have their own readme, I want to centralise all the information in one place to make it easier to navigate and find information on my GitHub profile.

## Docker

- Docker tools (https://github.com/JBongars/docker-tools)
  - Current implementation is bulky and requires the user to clone the repository. Also building docker images is slow. Some additional features I want to work on:-
    - [ ] Fix annoying backgrounding issue.
      - When you press C+z to background a process in a docker container, it backgrounds the process on the host machine. Maybe there is a way to do this? If not, I already found a workaround by using tmux but it would be nice to have this feature.
    - [ ] Universal Copy/Paste
      - I found this repo https://github.com/ms-jpq/isomorphic_copy. It's fine but it uses bash to launch docker. Also it looks like it only works in Linux? So might need to adapt to work on Windows.
    - [ ] Add support for following:-
      - [ ] gcp
      - [ ] Azure
    - [ ] Instead of building everything in the base configuration (vim/zsh/python/etc...) allow the user to select what they want to install.
    - [ ] Install and configure a really good neovim configuration to use. Should have integration with copilot and auto completion. Come up with a good workflow
    - [ ] Play with noVNC to build images for following:-
      - [ ] Postman
      - [ ] Firefox
      - [ ] Transmission/Deluge
      - [ ] PgAdmin
      - [ ] VSCode (maybe?)
    - [ ] As above, but might be a bit more difficult:-
      - [ ] Quake 2 (This game is open source so could be a good proof of concept for supporting other games)
      - [ ] Diablo 2 (For personal use only as don't want to get sued by Blizzard)
  - Learn Kubernetes (the hard way) - https://github.com/kelseyhightower/kubernetes-the-hard-way

## IaC

- Private VPN
  - Use an ansible playbook to deploy a AWS EC2 instance with OpenVPN installed and configured. The playbook will also generate a client certificate and key pair for the user to download and use to connect to the VPN.
- Private VPS connected using VNC/noVNC (Linux)
  - Ansible playbook like the above except it will install Ubuntu/Arch/Debian and install a VNC server and noVNC to allow the user to connect to the VPS using a web browser. This can also be accomplished by using a docker container. Pros of this approach is that it can be generalized to use any Docker Tools container.
- Private VPS connected using RDP (Windows) (maybe)
  - This might be a bit more difficult than above.
