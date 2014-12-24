## Info

Gera uma box [Debian](https://www.debian.org/) Vanilla (sem pacotes extras instalados) utilizando o [Packer](https://packer.io/) para o desenvolvimento de projetos da Comunidade Mozilla Brasil.

## Configuração da Box

**Sistema Operacional:** Debian 7.7.0 amd64 - (netinst)

**HD:** 32 GB

**RAM:** 512 MB

**CPU:** 1

**Pacotes pré-definidos:** openssh-server sudo bzip2 acpid cryptsetup zlib1g-dev wget curl dkms make nfs-common git rsync

**Localidade:** pt_BR.UTF-8

**Teclado:** br-abnt2

**Timezone:** America/Sao_Paulo



## Gerando a box com Packer

É obrigatório definir a versão do Debian e a assinatura checksum sha512 para gerar a imagem do VirtualBox.

Edite o arquivo **mozilla-brasil-packer-debian** alterando as variáveis conforme desejado:
```
    "variables": {
        "debian_version": "7.7.0",
        "iso_checksum": "5cb6e4fea55fbb5173f90c3a545b843c6c193e29c3aa32b3306c9bbdfb1ad6a6a36ae8be50e91af9d03d5f21c472bd05d04d3508172e0b519e76714333c7c74b"
    },

```

Depois de editar, insira o comando para criar a box:
```
packer build mozilla-brasil-packer-debian
```

É isso aí! :)

Basta add a box gerada no seu vagrant e começar a trabalhar...


### Box Finalizada

Você pode fazer o download desta box. [aqui](http://lab.cynthiapereira.com/mozilla-brasil/mozilla-brasil-packer-debian-7.7.0-amd64_virtualbox.box)


## Créditos e Licença

Inspirado no: [deimosfr/packer-wheezy](https://github.com/deimosfr/packer-wheezy)

Licença: [GPL2](LICENSE)
