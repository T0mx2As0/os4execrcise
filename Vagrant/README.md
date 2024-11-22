README file Modulo formativo

I tools vengono utilizzati sono:
Vagrant, Ansible, Prometheus, Grafana, Haproxy, Podman

Dipendenze:
Vagrant e Ansible devo essere installati sulla macchina dalla quale faremo vagrant up.

Fare il clone del progetto in una qualsiasi cartella del PC.
Spostarsi all'interno della cartella sou-lab-cni/Vagrant, dove è presente un file chiamato Vagrantfile.

All'interno di quella cartella troveremo:

- Vagrantfile -> Il file Vagrantfile è un file di configurazione utilizzato da Vagrant per definire come creare, configurare e gestire le macchine virtuali, scritto in Ruby
- main_playbook.yml -> Playbook ansible che verra eseguito una volta che le VMs saranno up & running.
- Cartella Roles -> sono i ruoli che saranno eseguiti da ansible. Abbiamo 3 ruoli,  sou_podman che si occupa dell'installazione sulle VMs di podam, Haproxy che fara partire un container su una delle due VM, il quale fara da ReverseProxy per i due container, Grafana e Prometheus, che verranno fatti partire dal terzo ruolo Monitor.

Dopo che ci siamo spostati all'interno della directory Vagrant possiamo lanciare il comando vagrant up.
