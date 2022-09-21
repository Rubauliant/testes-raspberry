# Ecossistema ML com RaspberyPi

## 1.0 Configurando o RaspberyPi:

Aqui vamos utilizar da forma remota para acesso ao dispositivo, o que dispensa o uso de um monitor e mouse externos. Pra isso, temos que criar a imagem num flashdisk (ssd ou pendrive) para servir de boot no RaspberyPi. Para esta etapa serão necessários:

- Um RaspberyPi 3 ou 4;
- Uma fonte de alimentação para o Pi de 5V
- Um pendrive ou um microSD;
- Um computador;
- Dedicação e calma

Abaixo está o passo a passo resumido retirado das referências:

### 1.0.1 Baixando o criador de imagem

Primeiramente baixamos o <a href=https://www.raspberrypi.com/software>criador de imagem e boot </a> para o raspbery PI. Existe para qualquer versão de sistema operacional.
Com isso podemos criar o boot pelo cartão sd.

### 1.0.2 Confiurando arquivos para headless mode
Para isso, você deve criar 2 arquivos dentro da raíz da pasta boot do flash disk com a imagem:

- Um chamado `ssh` sem extensão para dizer que deve ser iniciado em headless mode;
- Outro chamado `wpa_supplicant.conf` que irá ter a seguinte estrutura dentro dele (dando a configuração para o local BR):
```
cntrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=BR
network={
    ssid="nome-da-rede-wifi"
    psk="senha-da-rede-wifi"
}
```
ambos arquivos devem ser salvos em um notepad, em que se quiser salvar sem extensão (como no caso do `ssh`), podemos colocar somente o nome entre asptas no momento de salvar o arquivo:

## 1.1 Configurando através de SSH:

Primeiramente, precisamos pingar o hostname do device de acordo com o que foi configurado. Para isso, precisamos usar um protocolo de SSH. com o Putty podemos fazer isso. Primeiramente, baixamos o executável na <a href=https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html>página oficial</a>, e depois executamos ela pelo terminal:

```
> ping rubaraspberrypi
```

