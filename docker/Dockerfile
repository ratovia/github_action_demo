FROM arm64v8/ubuntu:22.04

COPY . /workspace

RUN apt update -y \
    && apt install ansible -y

WORKDIR /workspace

CMD bash -c "uname -a && ansible-playbook ansible/playbook.yml --connection=local && uname -a"
