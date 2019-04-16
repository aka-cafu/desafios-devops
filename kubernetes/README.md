# Desafio 02: Kubernetes

## Motivação

Este exemplo foi criado utilizando o [minikube](https://kubernetes.io/docs/setup/minikube/), para que seja possível executa-lo em um cluster não gerenciado pelo minikube, é necessário alterar alguns passos no [script de inicialização](https://github.com/aka-cafu/desafios-devops/blob/master/kubernetes/minikube-deploy-with-helm.sh).

A inicialização da aplicação de se dá com as informações, que são preenchidas no arquivo [values.yaml](https://github.com/aka-cafu/desafios-devops/blob/0.2/kubernetes/idwall-app/values.yaml), como nome da aplicação, porta do container, nome da imagem, tag, etc.


## Dependências
Para que seja possível executar o projeto utilizando o minikube, é preciso baixá-lo, juntamente com o [kubectl]() e também é preciso ter um virtualizador ([Virtualbox](https://www.virtualbox.org/wiki/Downloads), [KVM](http://www.linux-kvm.org/), [VMware](https://www.vmware.com/products/fusion), etc) em sua instância/notebook.

* Instalação do _kubectl_: https://kubernetes.io/docs/tasks/tools/install-kubectl/
* Instalação do Minikube: https://kubernetes.io/docs/tasks/tools/install-minikube/


**Obs:** Antes de iniciar o processo de deploy, através do script, execute o comando abaixo para capturar o endereço ip do seu cluster e inclua a seguinte entrada no seu arquivo **/etc/hosts/**

```bash
minikube ip
192.168.100.1
```

Entrada no **/etc/hosts**
```bash
192.168.100.1 hello-idwall.challenge
```

## Execução 

Para realizar o deploy da aplicação, no diretório raiz execute o script [minikube-deploy-with-helm.sh](https://github.com/aka-cafu/desafios-devops/blob/master/kubernetes/minikube-deploy-with-helm.sh)

```bash
./minikube-deploy.sh
```

## Demo
![asciinema_record](http://i.imgur.com/GzH6R4U.gif)