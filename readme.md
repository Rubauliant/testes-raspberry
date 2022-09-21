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

## 1.1 Configurando através de SSH:

Primeiramente, precisamos pingar o hostname do device de acordo com o que foi configurado. Para isso, precisamos usar um protocolo de SSH. com o Putty podemos fazer isso. Primeiramente, baixamos o executável na <a href=https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html>página oficial</a>, e depois executamos ela pelo terminal:

```
> ping ruba-raspberrypi.local
```

