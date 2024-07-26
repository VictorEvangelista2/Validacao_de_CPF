# Validações em JavaScript 

# Introdução 

### Desenvolver uma aplicação web simples utilizando JavaScript para validar a formatação e a integridade de números de CPF e endereços de email inseridos pelo usuário. 
### Também Definir detalhadamente as regras de validação para CPF e email, considerando os padrões de formato de email, Essas regras para validação será apresentadas futuramente nos capítulos deste arquivo README.

# Desenvolvimento 

### Mensagens de erro personalizadas: Exibe mensagens claras e concisas para cada tipo de erro, facilitando a compreensão do usuário.
### O código desenvolvido pode ser adaptado e reutilizado em outros projetos, agilizando o desenvolvimento.

# Recursos JS utilizados no projeto ChecarEmail

### A função checarEmail() tem como objetivo validar se um endereço de email inserido em um formulário HTML é válido. Ela verifica a presença do símbolo "@" e de pelo menos um ponto "." no endereço de email.
![Screenshot_20240726-072144](https://github.com/user-attachments/assets/1cbef852-a31a-45fd-b2c8-f95d173583f2)

 - **Verificação de Campo Vazio:** document.forms[0].email.value == "": Verifica se o campo de email está vazio. Se estiver, a função retorna false, indicando que o email não é válido.
 - **Verificação da Presença do "@":** document.forms[0].email.value.indexOf('@') == -1: Verifica se o símbolo "@" não está presente no endereço de email. Se não estiver, a função retorna false.
 - **Verificação da Presença do ".":** document.forms[0].email.value.indexOf('.') == -1: Verifica se o ponto "." não está presente no endereço de email. Se não estiver, a função retorna false.
 - **Exibição de Mensagem de Erro:** Se alguma das condições acima for verdadeira, a função exibe uma mensagem de alerta informando que o email é inválido.
 - Se todas as condições forem falsas (ou seja, o email é válido), a função retorna false.

# Recursos JS utilizados no projeto ChecarCpf()

 - O código permite que um usuário digite um CPF em um formulário e, ao enviar o formulário, verifica se o CPF é válido de acordo com as regras implementadas na função validarCPF. O resultado da validação é exibido para o usuário em forma de mensagem com cores diferentes para indicar se o CPF é válido ou não.

![Screenshot_20240726-074241](https://github.com/user-attachments/assets/f8584b86-68f1-4133-8155-793cb27c939c)

 - **event.preventDefault()**: Impede que o formulário seja enviado para o servidor de forma padrão, o que permitiria que o código JavaScript manipule a validação.
 - **Exibindo a Mensagem:** Se o CPF for válido, a mensagem "O CPF é válido!" é exibida em verde. Se o CPF for inválido, a mensagem "O CPF é inválido!" é exibida em vermelho.
 - **Adicionar um ouvinte de evento:** O addEventListener permite que o código responda a eventos, como o envio de um formulário.
 - Chamar uma função de validação: O código chama uma função externa validarCPF para realizar a lógica de validação do CPF.
 - A função validarCPF tem como principal objetivo verificar se um número de CPF (Cadastro de Pessoas Físicas) fornecido como parâmetro é válido de acordo com as regras de validação do CPF brasileiro.

![Screenshot_20240726-075124](https://github.com/user-attachments/assets/acd47ac7-1092-4887-9dd4-54a63f700609)

- **Remoção de Caracteres Não Numéricos:**
    cpf = cpf.replace(/[^\d]+/g, '');: Essa linha remove qualquer caractere que não seja um dígito do número de CPF, garantindo que apenas números sejam utilizados na validação.
  - **Verificação da Quantidade de Dígitos e Dígitos Iguais:**
   * if (cpf.length !== 11 || /^(\d)\1{10}$/.test(cpf)) { return false; }: Verifica se o CPF tem exatamente 11 dígitos. Verifica se todos os dígitos são iguais (um CPF válido não pode ter todos os dígitos iguais).
  - **Cálculo do Primeiro Dígito Verificador:**
   * Um loop for é utilizado para percorrer os primeiros 9 dígitos do CPF.
   * A cada iteração, o dígito é multiplicado por um peso (11-i), onde i é o índice do dígito.
   * Os resultados das multiplicações são somados.
   * O resto da divisão dessa soma por 11 é calculado.
   * Se o resto for 10 ou 11, ele é substituído por 0.
   * O resultado do cálculo é comparado com o décimo dígito do CPF fornecido. Se forem diferentes, o CPF é inválido.
   
