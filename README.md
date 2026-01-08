# Exercício 2 – Servidor DHCP na Azure com Terraform e Ansible

## Objetivo
O objetivo deste exercício foi criar automaticamente uma máquina virtual Linux na Microsoft Azure que desempenha o papel de **servidor DHCP**, utilizando **Terraform** para o provisionamento da infraestrutura e **Ansible** para a configuração do serviço, sem qualquer intervenção manual.

---

## Tecnologias Utilizadas
- Microsoft Azure
- Terraform
- Ansible
- Linux (Ubuntu 22.04)
- ISC DHCP Server
- Git e GitHub

---

## Descrição da Solução

1. Utilizando **Terraform**, foi criada uma infraestrutura na Azure que inclui:
   - Um Resource Group na região **Norway East**
   - Uma Virtual Network e Subnet
   - Um Network Security Group com acesso SSH
   - Uma máquina virtual Linux (Ubuntu)

2. A autenticação na máquina virtual é feita exclusivamente através de **chave SSH**, não sendo utilizada qualquer password nos ficheiros.

3.
