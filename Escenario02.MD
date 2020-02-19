# Escenario 2
## Estudiantes
Jorge Moreno - Andres Varela - Leonardo Zambrano

Para este escenario se identifican 3 etapas principales:

En la primera de este escenario, se realiza la creación de una única máquina utilizando Vagrant en la carpeta 00-Single-Machine. Posteriormente, por medio de Vagrant se genera un nuevo ambiente con multiples servidores en 01-Multiple-Machine. Por último, se genera un ambiente con multiples máquinas con vagrant, aprovisionados como servidores web y de base de datos por medio de Ansible.

### Procedimiento
# 00-Single-machine
1. Para definir la configuración de Vagrant, se establece el archivo VagrantFile, incluyendo en esta el sistema operativo centos 7, su hostname, y una dirección ip de su red.

![Vagrant File](/images/00-VagrantFile.PNG)

Se verifica el estado de la máquina de vagrant, que se encuentran por ahora inactivas.

![Vagrant Status](/images/00-vagrantstatusapagada.PNG)

2. Para encender la máquina, se utiliza el comando vagrant up, ubicados desde la carpeta en la cual se encuentra el archivo VagrantFile

![Vagrant Status](/images/00-vagrantup.PNG)

Una vez se ha ejecutado este procedimiento correctamente, se puede verifica que el estaod en que se encuentra la máquina ahora es "en ejecución".

![Vagrant Status](/images/00-vagrantstatusprendida.PNG)

3. Ahora, es posible acceder a la máquina mediante ssh desde el terminal de la máquina real en visualstudiocode, creando previamente un par de llaves de autenticación mediante el comando ssh-keygen:

![Vagrant Status](/images/00-vagrantssh.PNG)

4. Finalmente, la máquina puede ser destruida para dejar de utilizarla y no dejar rastro de ella, o recursos de vagrant utilizandose sin necesidad mediante el comando vagrant destroy.

![Vagrant Status](/images/00-vagrantdestroy.PNG)

# 01-Multiple-machines

Este es el archivo vagrantfile, mediante el cual se crean las máquinas con sistema operativo Centos7, asignando su dirección ip, memoria RAM, y CPUs.

![Vagrant Status](/images/01-vagrantfile.PNG)

Se verifica que las maquinas se encuentran creadas más no activas.

![Vagrant Status](/images/01-vagrantstatusapagadas.PNG)

 Ahora pueden encenderse ambas maquinas, y puede observarse todo el proceso que realiza vagrant para esto:
 
![Vagrant Status](/images/01-vagrantupa.PNG)
![Vagrant Status](/images/01-vagrantupb.PNG)

Las máquinas se encuentran ahora ejecutandose:

![Vagrant Status](/images/01-vagrantstatusprendidas.PNG)

Tambien puede accederse a ambas mediante ssh:

![Vagrant Status](/images/01-vagrantssh.PNG)

AL igual que en el caso anterior, se destruyen las maquinas en ejecución:

![Vagrant Status](/images/01-vagrantdestroy.PNG)


![Vagrant Status](/images/02-vagrantfilepartea.PNG)
![Vagrant Status](/images/02-vagrantfileparteb.PNG)
![Vagrant Status](/images/02-hosts.PNG)
![Vagrant Status](/images/02-ansiblecfg.PNG)
![Vagrant Status](/images/02-playbookpython.PNG)
![Vagrant Status](/images/02-playbookservers.PNG)
![Vagrant Status](/images/02-vagrantstatusprendidas.PNG)
