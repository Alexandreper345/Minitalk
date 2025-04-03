# 📡 Minitalk

O **Minitalk** é um projeto que explora a comunicação entre processos usando sinais Unix. O objetivo é criar um cliente e um servidor que possam trocar mensagens de forma eficiente e confiável.

---

## 📌 Índice

- [Objetivo do Projeto](#-objetivo-do-projeto)
- [Funcionamento](#-funcionamento)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Instalação](#-instalação)
- [Como Usar](#-como-usar)
- [Testes](#-testes)
- [Contato](#-contato)

---

## 🎯 Objetivo do Projeto

O **Minitalk** foi desenvolvido para demonstrar o uso de sinais Unix (`SIGUSR1` e `SIGUSR2`) para comunicação entre processos. O servidor recebe mensagens enviadas pelo cliente, bit a bit, e exibe a mensagem na saída padrão.

---

## 🔧 Funcionamento

O projeto é composto por dois programas principais:

- **Servidor:** Aguarda conexões do cliente e recebe os sinais correspondentes aos caracteres da mensagem.
- **Cliente:** Envia uma string para o servidor, transformando cada caractere em uma sequência de sinais `SIGUSR1` e `SIGUSR2`.

Fluxo de funcionamento:
1. O servidor é iniciado e exibe seu PID.
2. O cliente é executado, enviando sinais ao servidor com a mensagem a ser transmitida.
3. O servidor interpreta os sinais recebidos e exibe a mensagem.

---

## 🛠 Tecnologias Utilizadas

- **Linguagem:** C  
- **Compilador:** `cc` (ou GCC, Clang)  
- **Sinais Unix:** `SIGUSR1` e `SIGUSR2`  
- **Sistema Operacional:** Linux, macOS  

---

## 🛠 Instalação

### 🔹 Passo 1: Clonar o repositório
```sh
git clone https://github.com/seu-usuario/minitalk.git
```

### 🔹 Passo 2: Compilar o projeto
```sh
cd minitalk
make
```

Isso gerará os executáveis `server` e `client`.

---

## 🚀 Como Usar

### 🔹 Passo 1: Iniciar o Servidor
Execute o servidor para obter seu PID:
```sh
./server
```
Saída esperada:
```sh
Servidor rodando... PID: 12345
```

### 🔹 Passo 2: Enviar uma Mensagem
No terminal, utilize o cliente para enviar uma mensagem ao servidor:
```sh
./client 12345 "Olá, mundo!"
```
Substitua `12345` pelo PID exibido pelo servidor.

Se tudo estiver correto, o servidor imprimirá a mensagem recebida:
```sh
Mensagem recebida: Olá, mundo!
```

---

## 🧪 Testes

### 🔹 Testes Manuais
- Verifique se o servidor exibe corretamente o PID ao ser iniciado.
- Envie mensagens com diferentes tamanhos para garantir a consistência.
- Teste com caracteres especiais para validar a transmissão correta.

---

## 📩 Contato

Se tiver alguma dúvida ou sugestão, entre em contato:
📧 **E-mail:** [asilvaperoba@gmail.com](mailto:asilvaperoba@gmail.com)

