# Validações em JavaScript 

# Introdução 

### Desenvolver uma aplicação web simples utilizando JavaScript para validar a formatação e a integridade de números de CPF e endereços de email inseridos pelo usuário. 
### Também Definir detalhadamente as regras de validação para CPF e email, considerando os padrões de formato de email, Essas regras para validação será apresentadas futuramente nos capítulos deste arquivo README.

# Desenvolvimento 

### Mensagens de erro personalizadas: Exibe mensagens claras e concisas para cada tipo de erro, facilitando a compreensão do usuário.
### O código desenvolvido pode ser adaptado e reutilizado em outros projetos, agilizando o desenvolvimento.

# Recursos JS utilizados no projeto ChecarEmail

### A função checarEmail() tem como objetivo validar se um endereço de email inserido em um formulário HTML é válido. Ela verifica a presença do símbolo "@" e de pelo menos um ponto "." no endereço de email.
 - ![Screenshot_20240726-072144](https://github.com/user-attachments/assets/1cbef852-a31a-45fd-b2c8-f95d173583f2)

 - **Verificação de Campo Vazio:** document.forms[0].email.value == "": Verifica se o campo de email está vazio. Se estiver, a função retorna false, indicando que o email não é válido.
 - **Verificação da Presença do "@":** document.forms[0].email.value.indexOf('@') == -1: Verifica se o símbolo "@" não está presente no endereço de email. Se não estiver, a função retorna false.
 - **Verificação da Presença do ".":** document.forms[0].email.value.indexOf('.') == -1: Verifica se o ponto "." não está presente no endereço de email. Se não estiver, a função retorna false.
 - **Exibição de Mensagem de Erro:** Se alguma das condições acima for verdadeira, a função exibe uma mensagem de alerta informando que o email é inválido.
 - Se todas as condições forem falsas (ou seja, o email é válido), a função retorna false.

# Recursos JS utilizados no projeto ChecarCpf()
