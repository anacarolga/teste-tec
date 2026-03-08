# teste-tec
Teste técnico Ana Caroline Galdino de Almeida Canholato

### Resultado QA:

Tela de Login
1. Título: Para email
Descrição: A palavra email está descrita incorretamente.
Passos para reproduzir: O correto seria e-mail, com hífen, de acordo com a ABL.
Resultado atual: EMAIL
Resultado esperado: E-MAIL
Severidade (Crítico / Alto / Médio / Baixo): Baixo
Prioridade (Alta / Média / Baixa): Baixa

Tela criação de conta

2. Título: Caixa de preenchimento vazado
Descrição: Quando em tela cheia, a caixa de preenchimento não está se adaptando ao espaço em caixa branca, centralizada na tela.
Passos para reproduzir: Ao abrir a tela de Criar conta, o layout já lista fora do padrão. Mas ao abrir o inspecionar, identificado que a partir da resolução 638.40px x 703.20, os campos estão no tamanho padrão.
Resultado atual: Somente campo EMAIL está com tamanho de preenchimento correto. Campos NOME, TELEFONE, SENHA E CONFIRMAR SENHA, para preenchimento de dados, está com tamanhos vazados do quadro branco centralizado.
Resultado esperado: Adaptar para tela cheia, acima de 738px, o espaço de preenchimento dos dados.
Severidade (Crítico / Alto / Médio / Baixo): Alta
Prioridade (Alta / Média / Baixa): Alta
Obs.: Link vídeo

3. Título: Campo TELEFONE permitindo mais de 11 caracteres
Descrição: Quando preenchido o campo TELEFONE, ESTÁ PERMITINDO MAIS DE 11 CARACTERES (ddd+900000000)
Passos para reproduzir: Clique no campo de preenchimento de dado telefone, e ao inserir os números, permite inserir além de 11 caracteres, que seria o valor máximo
Resultado atual: Quantidade de caracterer livre, possibilitando erro do usuário
Resultado esperado: Travar em 11 caracteres, para evitar preenchimento incorreto.
Severidade (Crítico / Alto / Médio / Baixo): Alto
Prioridade (Alta / Média / Baixa): Média

4. Título: Senhas diferentes
Descrição: Permitido criar conta com senhas diferentes
Passos para reproduzir: Inserido dado ana12345 no campo SENHA e inserido dado ana12346 no campo CONFIRMAR SENHA e foi aceito.
Resultado atual: Permitido criar conta com valores de senha diferentes, sem apresentar erro.
Resultado esperado: Ao ser identificado valores diferentes, apresentar erro na tela e na api.
Severidade (Crítico / Alto / Médio / Baixo): Crítico
Prioridade (Alta / Média / Baixa): Alta

5. Título: Caractere especial
Descrição: Permitido criar conta com senha sem caractere especial, diverge da regra de negócio na descrição do campo.
Passos para reproduzir: Inserido dado ana12345 no campo SENHA, sem inserir caractere especial.
Resultado atual: Permitido criar conta sem inserir valor de senha ou confirmar senha com caracterer especial, como descrito como regra de negócio.
Resultado esperado: Api realizar validação de dado inserido, retornando erro ao tentar criar conta.
Severidade (Crítico / Alto / Médio / Baixo): Alto
Prioridade (Alta / Média / Baixa): Alto

Tela simples de sucesso

6. Título: Erro inesperado_1
Descrição: Ao realizar login, apresentou flag Erro inesperado
Passos para reproduzir: Na tela de login, após cadastro de conta, inserido e-mail e senha ana12345
Resultado atual: Apresentado login com sucesso, porém com uma flag de Erro inesperado na tela. Ao inspecionar, não foi encontrado error de api.
Resultado esperado: Sem erro de console, não apresentar flag de Erro inesperado e validar Login realizado com sucesso.
Severidade (Crítico / Alto / Médio / Baixo): Alto
Prioridade (Alta / Média / Baixa): Alto

7. Título: Erro inesperado_2
Descrição: Ao realizar login, apresentou flag Erro inesperado
Passos para reproduzir: Na tela de login, após cadastro de conta, inserido e-mail e senha ana12345. Ao abrir o console, não realizado nenhuma chamada de integração
Resultado atual: Apresentado login com sucesso, porém com uma flag de Erro inesperado na tela. Ao inspecionar, não foi encontrado error de api.
Resultado esperado: Api entregar erro no console, descrevendo motivo de erro (integração, security, dado incorreto)
Severidade (Crítico / Alto / Médio / Baixo): Crítico
Prioridade (Alta / Média / Baixa): Alta

Resultado final

8. Quais 2 bugs você corrigiria primeiro e por quê?
   
Bug 4 e 7.
Ambos foram classificados como Severidade Crítico e prioridade Alta.
O erro 4 afeta principalmente segurança da plataforma, integração com api, ou seja, não foi realizado uma correta construção de back-end.
O erro 7, por não apresentar o motivo de erro, dificulta de realizar leitura do erro, de aplicar suporte ou correção, sendo obrigada a realizar debug de todo back-end.

9. Caso tenha, coloque suas sugestões de melhorias para essas telas.
    
Inicialmente, aplicaria melhoria de inserir a flag de erro para o topo da tela, canto direito. De acordo com UX, é o caminho mais "fácil" do usuário visualizar, por hábito de demais aplicações esse layout.

## Vídeo BUG 2:

https://github.com/user-attachments/assets/ff2853c2-91b1-446a-97bf-98d839eacb09


##

