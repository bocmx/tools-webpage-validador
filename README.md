# tools-webpage-validador
Validador de condições pré-definidas (ex: e-mail de alunos) utilizando o n8n como backend.

Este projeto consiste em uma página HTML com um campo de entrada para valores (como e-mails de alunos). Após o preenchimento, o valor é enviado via Webhook para um workflow no **n8n**, que processa a requisição e retorna um código de status. Se a resposta for *200*, um script de redirecionamento é acionado, levando o usuário para a página desejada.

## Como implementar
1. Copie o JSON do workflow disponível na pasta backend-n8n.

2. Importe o JSON para sua instância do n8n.

3. Gere o endpoint do Webhook correspondente e atualize o valor na página HTML com esse endpoint.
