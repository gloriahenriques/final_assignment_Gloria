# Exercício 1 – Terraform e Ansible na Azure

## Objetivo
O objetivo deste exercício foi criar automaticamente uma máquina virtual Linux na Microsoft Azure utilizando **Terraform**, e posteriormente configurar essa máquina com **Ansible** para servir uma página web através do **NGINX**, sem qualquer configuração manual.

---

## Tecnologias Utilizadas
- Microsoft Azure
- Terraform
- Ansible
- Linux (Ubuntu 22.04)
- NGINX
- Git e GitHub

---

## Descrição da Solução

1. Foi criado um **Resource Group** na região **Norway East**, que é a única região funcional nesta conta Azure.
2. Utilizando Terraform, foi criada:
   - Uma Virtual Network
   - Uma Subnet
   - Um Network Security Group com regras para SSH (22) e HTTP (80)
   - Uma máquina virtual Linux (Ubuntu)
3. A autenticação na máquina é feita através de **chave SSH**, não sendo utilizada qualquer password.
4. Após a criação da máquina, foi utilizado **Ansible** para:
   - Atualizar o sistema
   - Instalar o NGINX
   - Ativar e iniciar o serviço
   - Criar um ficheiro `index.html` personalizado servido pelo NGINX

---

## Segurança
- Não existem passwords guardadas nos ficheiros Terraform ou Ansible
- A autenticação SSH é feita com chave pública
- Ficheiros sensíveis e temporários do Terraform (`.terraform`, `.tfstate`) estão excluídos do repositório através do `.gitignore`

---

## Estrutura do Projeto

