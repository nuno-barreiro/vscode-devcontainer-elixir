FROM elixir:1.13.4-alpine

RUN apk update \
    && apk add openssh \
    && apk add openssl \
    && apk add --no-cache git \
    # Install ZSH & OhMyZsh for development inside container
    && apk add --no-cache zsh \
    && apk add zsh-vcs \
    && sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

COPY .zshrc /root/.zshrc

RUN mix --version