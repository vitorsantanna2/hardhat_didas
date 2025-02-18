# **Zeniq - ecomap**

## **Descrição**

Este projeto é um contrato inteligente simples escrito em Solidity chamado ecomap que serve para registrar informacoes na blockchain. O projeto utiliza o ambiente de desenvolvimento Hardhat.

## **Índice**

- **[Pré-requisitos](https://chat.openai.com/c/c9518ab3-74e3-4fbf-9cf1-d646b9210b11#pr%C3%A9-requisitos)**
- **[Instalação](https://chat.openai.com/c/c9518ab3-74e3-4fbf-9cf1-d646b9210b11#instala%C3%A7%C3%A3o)**
- **[Configuração](https://chat.openai.com/c/c9518ab3-74e3-4fbf-9cf1-d646b9210b11#configura%C3%A7%C3%A3o)**
- **[Compilação](https://chat.openai.com/c/c9518ab3-74e3-4fbf-9cf1-d646b9210b11#compila%C3%A7%C3%A3o)**
- **[Deploy](https://chat.openai.com/c/c9518ab3-74e3-4fbf-9cf1-d646b9210b11#deploy)**
- **[Execução de Testes](https://chat.openai.com/c/c9518ab3-74e3-4fbf-9cf1-d646b9210b11#execu%C3%A7%C3%A3o-de-testes)**
- **[Interagindo com o Contrato](https://chat.openai.com/c/c9518ab3-74e3-4fbf-9cf1-d646b9210b11#interagindo-com-o-contrato)**

## **Pré-requisitos**

- Node.js e npm: Você pode baixá-los **[aqui](https://nodejs.org/)**.

## **Instalação**

1. **Clonar o Repositório**:
    
    ```bash
    git clone https://github.com/diegofornalha/zeniq.git
    ```
    
2. **Navegar até o Diretório do Projeto**:
    
    ```bash
    cd zeniq
    ```
    
3. **Instalar Dependências**:
    
    ```bash
    npm install
    ```
    

## **Truffle Dashboard**

Para abrir o Truffle Dashboard, você pode executar o seguinte comando:

```bash
sudo truffle dashboard
```

## **Deploy com Truffle Dashboard**

Para fazer o deploy do contrato usando o Truffle Dashboard, execute o seguinte comando:

```bash
sudo npx truffle run scripts/deploy.js --network truffleDashboard
```

## **Configuração do `.env`**

1. Crie um arquivo **`.env`** no diretório raiz do projeto.
2. Adicione a chave privada e outras variáveis de ambiente necessárias.
    
    **Exemplo de `.env`**:
    
    ```
    PRIVATE_KEY=0xSuaChavePrivadaAqui
    ```
    
    **Nota**: Certifique-se de que este arquivo não seja incluído no controle de versão.
    

## **Compilação**

Para compilar o contrato, execute o seguinte comando:npx hardhat compile

```bash
sudo npx hardhat compile
```

## **Deploy**

Para fazer o deploy do contrato, execute o seguinte comando:

```bash
sudo npx hardhat run scripts/deploy.js
```

O endereço do contrato implantado será exibido no console.

## **Execução de Testes**

Para executar os testes, use o seguinte comando:

```bash
sudo npx hardhat test
```

## **Interagindo com o Contrato**

Você pode usar o script **`distribute.js`** para interagir com o contrato:

```bash
sudo npx hardhat run scripts/distribute.js
```

---

## **Deploy na Rede Zeniq**

Para fazer o deploy do contrato na rede Zeniq, execute o seguinte comando:

```bash
sudo npx hardhat run scripts/deploy.js --network zeniq
```

Execute o seguinte comando para interagir com o contrato:

```bash
sudo npx hardhat run scripts/distribute.js --network zeniq
```

Isso executará o script e interagirá com o contrato implantado na rede Zeniq.

### **Removendo Artefatos e** truffle

1. **Remover a Pasta de Artefatos**
    
    ```bash
    sudo rm -rf build/
    ```
    
2. **Instalar Dependências**
    
    ```bash
    sudo npm install
    ```
    
3. **Compilar Contratos**
    
    ```bash
    sudo truffle compile
    ```
    
4. **Implantar Contratos**
    
    ```bash
    sudo truffle migrate --reset
    ```
    
5. **Executar Testes (Opcional)**
    
    ```bash
    sudo truffle development
    ```
    
    ### **Migre os Contratos**
    
    Agora você pode migrar seus contratos para a rede de desenvolvimento.
    
    ```bash
    sudo truffle migrate --network development
    ```
    
    O flag **`--network development`** especifica que você deseja usar as configurações da rede de desenvolvimento definidas no seu **`truffle-config.js`**.
    
    ### **Teste os Contratos (Opcional)**
    
    Se você tiver testes escritos, você pode executá-los para garantir que tudo está funcionando como esperado.
    
    ```bash
    sudo truffle development
    ```
    
    Esses comandos devem implantar seus contratos na rede de desenvolvimento local configurada pelo Ganache. Certifique-se de que o Ganache está rodando e acessível para que esses comandos funcionem como esperado.
