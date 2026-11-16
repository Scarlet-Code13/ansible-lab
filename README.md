# Laboratorio de Ansible con Docker

## Descripción
En esta práctica se realizó la configuración de un entorno de automatización utilizando Ansible y Docker. Se crearon dos servidores Ubuntu para administrar y ejecutar tareas de manera remota.

## Herramientas utilizadas
- Ubuntu 24.04
- Docker
- Docker Compose
- Ansible
- Python 3.12.3
- SSH

## Estructura del proyecto

- docker-compose.yml: configuración de los contenedores.
- inventory.ini: inventario de los servidores.
- playbook.yml: automatización de tareas.
- README.md: documentación del proyecto.

## Configuración realizada

Se crearon dos contenedores:
- server1 (puerto SSH 2221).
- server2 (puerto SSH 2222).

Se instaló Python y se configuró SSH en ambos servidores para permitir la conexión desde Ansible.

## Pruebas realizadas

1. Verificación de la versión de Python.
2. Comprobación de conexión mediante el módulo ping.
3. Ejecución del comando hostname.
4. Ejecución del comando python3 --version.
5. Creación y ejecución de un Playbook.
6. Creación de un directorio llamado practica-ansible en ambos servidores.

## Ejecución del Playbook

Para ejecutar el Playbook se utilizó:

    ansible-playbook -i inventory.ini playbook.yml

## Verificación de conexión

    ansible all -i inventory.ini -m ping

## Resultados

La práctica finalizó correctamente. Ambos servidores respondieron satisfactoriamente a las pruebas de conexión y ejecutaron las tareas automatizadas mediante Ansible.

Se comprobó que el directorio practica-ansible fue creado correctamente en ambos contenedores.

## Conclusión

Mediante esta práctica aprendí a configurar servidores con Docker, establecer conexiones SSH y utilizar Ansible para automatizar tareas en múltiples servidores. También comprendí cómo funcionan los inventarios y los Playbooks dentro de Ansible.
