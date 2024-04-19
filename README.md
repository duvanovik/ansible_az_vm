# Ansible Azure VM by Duvan Garcia

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
   
2. Ejecute el siguiente comando:
    ```bash
     chmod 775 .
El cual permite establecer los permisos de lectura, escritura y ejecución que seran utiles para el desarrollo de este proyecto.

3. Ejecutar el comando:
   ```bash
     ansible-playbook -i inventory/hosts.ini playbooks/install_docker.yml
este comando ejecuta el playbook install_docker.yml, que está ubicado en la carpeta playbooks, en los servidores definidos en el archivo de inventario hosts.ini. Este playbook contiene las instrucciones necesarias para instalar Docker en los servidores remotos.
![ansible1](https://github.com/duvanovik/ansible_az_vm/assets/42594511/09b388c4-c1a5-403d-b2be-a95fce7f7414)

4. Correr el contenedor:
   Ejecutar el comando:
   ```bash
     ansible-playbook -i inventory/hosts.ini playbooks/run_container.yml
![ansible2](https://github.com/duvanovik/ansible_az_vm/assets/42594511/0583fa70-93fa-4615-8175-3da0cf51b482)

5. Configurar la regla que me permita hacer port forward en mi VM.
   - Nos dirijimos a la máquina virtual en el portal de azure
   - Luego entramos a la configuración de red.
   - Cree una nueva ACL para el puerto. Indicamos el puerto en el que se está ejecutando el servicio. No modificamos la configuración por defecto.

![ansible3](https://github.com/duvanovik/ansible_az_vm/assets/42594511/3b53d2ea-3839-414d-868d-94acf5d11701)

6. Diviertase jugando Mario :)
 ![ansible4](https://github.com/duvanovik/ansible_az_vm/assets/42594511/723a0b48-f179-4f84-adca-7a68e6ee9a3c)
  
