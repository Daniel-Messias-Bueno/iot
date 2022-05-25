# Projeto de Irrigação Inteligente - IOT

Este projeto visa desenvolver um sistema de irrigação inteligente, utilizando os conceitos de IOT,nele serão implementados conceitos de Controle, Automação, IoT, programação em C++.

---
## 📄  Objetivo e uso do Projeto
Para esta automação, foram utilizados componentes de conexão com a internet, com a Placa ESP32 que faz conexão com o Broker Mosquitto, onde são estabelecidas as configurações do Broker. Além desse componente, foram utilizados, um transistor para ligar e desligar a bomba, um sensor de umidade de solo Higrômetro, para constatar a situação do solo, um diodo, um resistor de 1K, uma bomba de irrigação e jumpers para alimentar a energia de cada um deles.
o Projeto consiste na utilização de um sensor de umidade no qual, estara realizando a leitura do solo, onde ao constatar que o solo necessita de irrigação, acionara de forma automatica a irrigação,  até que chegue a umidade adequada.
As informações poderam ser acessadas em um dispositivo móvel, atráves de um app, onde podera também ser acionado a bomba d'água de forma remota.

---

## 🚀 Componentes Utilizados
- 1 Mini Bomba de Diafragma 12VDC RS385
- 1 Protoboard 830 Pontos MB-102 Solderless Breadboard
- 1 Sensor de Umidade do Solo Modulo + Sonda Higrômetro
- 1 Diodo Retificador 1N4007
- 1 Resistor 1K (1/4W)
- 1 Transistor NPN TIP122
- 1  Placa ESP32 WiFi / Bluetooth DEVKit V1 30 Pinos
- Magueiras de 1/4"
- Fonte de 12V
- Fonte de 9V
- vasilhas de plástico
- Jumpers

### ⚙️Requisitos do Projeto
     Aqui neste repositório também possui a programação do projeto em formato .ino e .txt e C++, que foi programado e desenvolvido no Software Arduino UNO, uma IDE que reconhece os componentes relacionados à automação e te permite configurá-los, programá-los e defini-los.

  - Instalar a IDE do Arduino (baixar no site: https://www.arduino.cc/en/software)
  






### 🔧 Instalação

**📋 Instruções para execução local**

- Após instalar a IDE do Arduino 
- baixar o código do GitHub para IDE
- Realizar a configuração de Rede Wi-fi no código (nome da rede e senha )
- Realizar o passo a passo, para montar o sistema, conforme o guia que consta nesse repositório
- Compilar o código, enviar o mesmo para a placa ESP32
- Baixar o App, MQTT DASH na play Store

- Após baixar o APP na Play Store
  - cadastrar o nome do seu servidor
  - cadastrar o endereço do broker, como exemplo o mosquitto ( test.mosquitto.org), que está sendo utilizado no projeto
  - cadastrar a porta , por padrão deixamos a 1883
  - clicar em salvar
  - clicar no sinal de + 
  - no campo name colocar um nome 
  - no campo topic,  assinar o nome do tópico, (este nome já está cadastrado no código)
  - clicar em salvar





### 🔧 Funcionamento

o sensor manda uma tensão, e essa tensão é transformada de valor analogico que vai de 0 a 4095, onde 4095 será 100% ,que será proporcional a umidade de 0 á 100%.
O transistor, nada mais é como se fosse um relé eletrônico,a porta D34 que está ligada a conexão base do transistor, o mesmo ao receber um nível alto nessa porta, o coletor do transistor
funcionara como um fio ligando o motor, e se colocarmos um nível baixo, o transistor funcionara como um contato aberto, ele separa as conexões dos fios, e o motor para de funcionar.
O papel do Diodo, ele deve ser utilizado no projeto, pois toda vez que ligamos o motor, ao ligar o motor.
Ele ira dar um tranco de tensão, em um curto espaço de tempo, onde isso com o tempo, pode queimar o motor, e assim colocamos o Diodo para proteger o motor, e impedir que isso aconteça 


