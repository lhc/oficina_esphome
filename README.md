# ESPHome - Oficina de IoT

## Introdução

ESPHome é uma ferramenta poderosa para criar firmwares personalizados para dispositivos ESP8266 e ESP32, facilitando a integração com sistemas como o Home Assistant. Nesta oficina, aprenderemos como configurar e utilizar o ESPHome para criar e gerenciar dispositivos IoT.

---

## Instalação do ESPHome

### Linux
Instale o ESPHome usando o `pip`:

```sh
pip install esphome
```

Verifique se a instalação foi bem-sucedida:

```sh
esphome --version
```

Saída esperada:

```
Version: 2025.2.2
```

### Windows
Baixe e instale o Python e, em seguida, instale o ESPHome com o comando acima.

---

## Criando um Novo Projeto com ESPHome
Para criar um novo projeto ESPHome, siga os passos abaixo:

1. Execute o assistente para criar um novo firmware:

```sh
esphome wizard meu_projeto.yaml
```

2. Siga as instruções interativas para:
   - Definir o nome do dispositivo
   - Escolher o modelo do microcontrolador (ESP32, ESP8266, etc.)
   - Selecionar a placa utilizada
   - Configurar a rede Wi-Fi
   - Definir uma senha de acesso

3. Para compilar e instalar o firmware:

```sh
esphome run meu_projeto.yaml
```

Esse comando compilará o código e o instalará no dispositivo conectado via USB.

---

## Especificando a Versão do ESPHome

Para garantir compatibilidade, é recomendável especificar a versão do ESPHome no arquivo de configuração YAML:

```yaml
esphome:
  name: meu_dispositivo
  platform: ESP32
  board: nodemcu-32s
  version: "2025.2.2"
```

---

## Recursos e Documentação
- [Documentação oficial do ESPHome](https://esphome.io/)
- [Componentes suportados pelo ESPHome](https://esphome.io/components/)
- [Lista de placas ESP32 suportadas](https://esphome.io/components/esp32)

---

## Dicas
- Se for utilizar conexão via Wi-Fi, assegure-se de estar na mesma rede que seu dispositivo ESP.
- Utilize um nome de dispositivo com apenas letras minúsculas, números e hífens para evitar erros.
- Se encontrar problemas ao compilar, tente atualizar as dependências com:

```sh
pip install --upgrade esphome platformio
```

---

## Conclusão

Esta oficina ira apresentou um guia básico para instalação e uso do ESPHome. A partir daqui, você pode explorar sensores, atuadores e outras funcionalidades para criar dispositivos IoT personalizados!

