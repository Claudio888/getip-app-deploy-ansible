# getip aplicação

Aplicação simples que exibe seu IP de acesso, feita visando apenas ser um detalhe para a implementação de IaC e conceitos de deployment blue/green

## Como usar

### Build

- Acesse o caminho /build-deploy/build em seguida execute o seguinte comando para chamar o playbook de construção da aplicação. 

Obs: Lembrando que neste passo ele ira executar localmente, por isto se faz necessário o Docker instalado

``` 
ansible-playbook -i hosts main.yml -vvv

```

### Deploy 

- Execute primeiramente a tarefa para copiar o arquivo "hosts" o nome é get-hosts

Obs: Lembre-se de alterar o ambiente e sua cor no caminho /vars/main.yml desta role, ira definir qual arquivo pegar

``` 
ansible-playbook -i hosts-local main.yml --tags "get-hosts-role"

```
- Execute agora a tarefa para fazer o deploy da aplicação no servidor

``` 
ansible-playbook -i hosts main.yml -vvv

```

## Backlog

- Implementar um projeto de CI com o Github Actions
- Deixar genéricos os caminhos no código todo
- Melhorar a forma de implementação/execução da role get-hosts

## Licença
[MIT](https://choosealicense.com/licenses/mit/)