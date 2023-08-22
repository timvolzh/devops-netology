## Задание 1

- Документрированность процессов. Скорость развертывания. Стандартизация шаблонов. 

- Идемпотентность - повторяемость и предсказуемость результата.

## Задание 2

- Ansible не требует развертывания на хостах, работает через ssh

- Я бы выбрал Push, т.к. контрольконфигураций осуществляется централизовано.



## Задание 3

>artem@a192:~$ vboxmanage --version
>6.1.46r158378
>artem@artemdev:~$ ansible --version
>ansible 2.10.8
>  config file = None
>  configured module search path = ['/home/artem/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
>  ansible python module location = /usr/lib/python3/dist-packages/ansible
>  executable location = /usr/bin/ansible
>  python version = 3.9.2 (default, Feb 28 2021, 17:03:44) [GCC 10.2.1 20210110]
>artem@artemdev:~$ vagrant -v
>Vagrant 2.2.14

## Задание  4

>vagrant@server1:~$ docker -v
> 
>Docker version 24.0.5, build ced0996
> 
> vagrant@server1:~$ docker ps
> 
>CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
 

---

Проблему
>ansible-playbook: error: unrecognized arguments: --sudo 

решил добавлением 
        setup.compatibility_mode = "2.0" вnode.vm.provision "ansible" do |setup|
        

