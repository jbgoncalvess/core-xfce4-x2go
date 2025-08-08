# Ambiente CORE + XFCE4 + X2Go com Ubuntu server 22.04

Este projeto disponibiliza um ambiente leve e funcional com o ***Common Open Research Emulator (CORE)*** instalado em um **Ubuntu Server 22.04**, utilizando a interface gráfica **XFCE4** e acesso remoto via **X2Go Server**.
Ele é ideal para simulações de redes em contextos educacionais, especialmente quando se dispõe de computadores com recursos limitados, permitindo acesso remoto prático e eficiente por meio do X2Go Client.

---

## Objetivo

Fornecer aos alunos do IFC – Campus Sombrio uma máquina virtual leve e eficiente para simulações de redes com o CORE, acessível graficamente via X2Go em qualquer computador, mesmo com hardware modesto.

---

## Tecnologias utilizadas

- Ubuntu - Server 22.04
- XFCE4 - Interface gráfica leve
- CORE - Common Open Research Emulator
- X2Go Server - Acesso remoto com interface gráfica

---

## Como usar

### 1. Baixe a máquina virtual `.ova`

> Link para download da máquina virtual:  
>[Disponível via Google Drive (4.3 GB)](https://drive.google.com/file/d/1-s3UP2AT2UPQnrGOwnAoFs8UUB9V5TCn/view?usp=drive_link)

---

### 2. Importe a máquina no VirtualBox

1. Abra o VirtualBox
2. Vá em **Arquivo > Importar Appliance**
3. Selecione o arquivo `.ova` baixado
4. Finalize a importação

---

### 3. Acessar a máquina via X2Go Client

1. **Instale o X2Go Client:**  

    >[Guia de instalação do X2Go Client](https://wiki.x2go.org/doku.php/doc:installation:x2goclient)  

2. **Crie uma nova sessão** no X2Go com as seguintes configurações:  
   - **Host:** *IP da máquina virtual*  
   - **Usuário:** `redes`
   - **Senha:** `123`    
   - **Tipo de sessão:** `XFCE`  

3. **Conecte-se** e utilize o ambiente gráfico remotamente.

---

### 4. Rodando o CORE

1. Após conectar via X2Go e abrir o ambiente gráfico, abra o **Terminal** e execute:

    ```bash
    sudo core-daemon
    ```
    >Esse comando inicializa o serviço do CORE responsável por gerenciar as simulações.
    >Deixe essa janela aberta enquanto utilizar o programa.

2. Em seguida, abra outro terminal e execute:

    ```bash
    core-gui
    ```

    >Isso abrirá a interface gráfica do CORE, onde você poderá criar, configurar e simular topologias de rede de forma interativa.


### 5. Documentação Utilizada

Para criar e configurar este ambiente, foram utilizadas as seguintes documentações oficiais:

- [Documentação do CORE](https://coreemu.github.io/core/)
- [Documentação do X2Go](https://wiki.x2go.org/doku.php/doc:start)
- [Documentação do XFCE4](https://docs.xfce.org/)
