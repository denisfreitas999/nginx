# NGINX

## Comandos do Nginx

Aqui estão alguns comandos comuns do Nginx e suas explicações:

### Comando para Recarregar o Servidor

- `nginx -s reload`: Recarrega o servidor Nginx. Este comando faz com que o Nginx recarregue sua configuração sem interromper o serviço. É útil quando você fez alterações na configuração e quer aplicá-las sem reiniciar o servidor.

### Ajuda e Versão

- `nginx -h` ou `nginx -?`: Mostra a tela de ajuda com uma lista de opções e saídas disponíveis.
- `nginx -v`: Mostra a versão do Nginx e sai.
- `nginx -V`: Mostra a versão do Nginx junto com as opções de configuração com que foi compilado, e então sai.

### Testar Configuração

- `nginx -t`: Testa a configuração do Nginx e sai. Este comando verifica a sintaxe do arquivo de configuração e reporta qualquer erro sem iniciar o servidor.
- `nginx -T`: Testa a configuração, imprime a configuração completa e então sai. Além de testar a sintaxe, este comando mostra a configuração completa, incluindo arquivos incluídos.

### Suprimir Mensagens

- `nginx -q`: Suprime mensagens não relacionadas a erros durante o teste de configuração. Este comando é útil quando você deseja ver apenas mensagens de erro.

### Enviar Sinal para o Processo Mestre

- `nginx -s signal`: Envia um sinal para o processo mestre do Nginx. Os sinais disponíveis são:
  - `stop`: Para o processo mestre imediatamente.
  - `quit`: Para o processo mestre graciosamente (após completar as conexões ativas).
  - `reopen`: Reabre os arquivos de log.
  - `reload`: Recarrega a configuração sem interromper o serviço.

### Configurações Adicionais

- `nginx -p prefix`: Define o caminho do prefixo (padrão: NONE). Este comando permite especificar um prefixo de caminho diferente para arquivos e diretórios do Nginx.
- `nginx -e filename`: Define o arquivo de log de erros (padrão: logs/error.log). Use este comando para especificar um arquivo de log de erros diferente.
- `nginx -c filename`: Define o arquivo de configuração (padrão: conf/nginx.conf). Este comando permite que você use um arquivo de configuração diferente do padrão.
- `nginx -g directives`: Define diretivas globais fora do arquivo de configuração. Este comando é útil para adicionar diretivas de configuração diretamente na linha de comando.

### Exemplo de Uso:

```sh
nginx -s reload       # Recarrega o servidor Nginx
nginx -t              # Testa a configuração e sai
nginx -V              # Mostra a versão e opções de configuração
nginx -c /path/to/nginx.conf  # Usa um arquivo de configuração específico
```