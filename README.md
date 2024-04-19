# Ansible Azure VM

Este repositorio contiene archivos para configurar y gestionar una máquina virtuale en Azure utilizando Ansible. En la cual se puede jugar Mario Broos a través de un contenedor de Docker.

## Contenido

- `playbooks/`: Carpeta que contiene los playbooks de Ansible para la configuración de las VMs.
- `inventory/`: Carpeta que contiene los archivos de inventario de Ansible.
- `scripts/`: Carpeta que contiene scripts auxiliares para el despliegue y gestión de las VMs.
- `README.md`: Este archivo, que proporciona información básica sobre el repositorio.

## Requisitos

- [Ansible](https://www.ansible.com/) instalado localmente.
- Una suscripción de Azure.
- Credenciales de Azure con permisos para crear y gestionar recursos de infraestructura.
- Una maquina virtual previamente configurada con ip pública y ssh habilitado con usuario y contraseña

## Uso

1. Clona este repositorio a tu máquina local:

   ```bash
   git clone https://github.com/duvanovik/ansible_az_vm.git
   
2. 