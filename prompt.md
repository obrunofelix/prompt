Crie um chatbot utilizando o framework Laravel 9 (PHP 8.1.10) que simule o jogo "Show do Milhão", respeitando o formato original do programa apresentado por Silvio Santos.

Este chatbot deve funcionar por etapas e conduzir o usuário da mesma forma que o jogo real, com perguntas de múltipla escolha e premiação progressiva.



✅ Especificações técnicas:

Framework: Laravel (versão Laravel 9 ).

Interface: Pode ser via terminal (Artisan command) ou via rota web simples (Blade ou API).

Banco de Dados: Use SQLite ou MySQL para armazenar perguntas e respostas.

Modelo de dados: Cada pergunta deve conter:

Enunciado

Quatro alternativas (A, B, C, D)

Resposta correta

Nível de dificuldade ou etapa (1 a 7, por exemplo)

Lógica do jogo:

O usuário começa na etapa 1 com uma pergunta fácil.

Cada acerto leva à próxima etapa (até 7 etapas).

Ao errar, o jogo termina com mensagem de encerramento.

O jogador pode "parar" a qualquer momento e levar o prêmio acumulado até então.

Exibir prêmios acumulados por etapa (ex: R$ 1 mil, R$ 5 mil, R$ 10 mil, etc).

Implementar ajuda dos universitários, cartas ou pular pergunta (opcional).

📋 Etapas do desenvolvimento:

Configuração inicial do projeto Laravel

Criar o projeto e configurar conexão com banco de dados.

Criação das migrations e seeders

Criar tabela questions com os campos descritos.

Popular com pelo menos 20 perguntas variadas (fáceis a difíceis).

Criação da lógica do jogo

Controlador para iniciar o jogo, exibir pergunta e aceitar resposta.

Validação da resposta e controle de progresso.

Sistema de pontuação/premiação

Associar cada etapa a um valor de prêmio.

Exibir mensagem de "você ganhou R$ X" ao finalizar.

Fluxo por etapas

Sempre após cada resposta, perguntar se o jogador quer:

Prosseguir para próxima etapa

Parar e levar o prêmio

(Opcional) Usar ajuda

Interface simples (opcional)

Criar uma rota e uma view Blade com botão para iniciar o jogo e interações simples.

🎮 Regras importantes:

O jogo só termina quando:

O jogador erra a resposta.

O jogador decide parar.

O jogador vence as 7 etapas.

Em cada etapa, o chatbot deve solicitar ação do usuário antes de prosseguir:

Mostrar pergunta e opções.

Esperar input (A, B, C, D ou Parar).

Responder com acerto/erro e valor ganho.

🧠 Exemplo de interação:



Etapa 1 – Prêmio: R$ 1.000Pergunta: Qual é a capital do Brasil?

A) São Paulo

B) Brasília

C) Rio de Janeiro

D) Belo HorizonteSua resposta: B

✅ Resposta correta!Você agora tem R$ 1.000Deseja continuar para a Etapa 2? (sim/parar)

Continue com esse fluxo até a última etapa.

Gere o código completo em Laravel, começando pela estrutura inicial, seguido das migrations, seeders e controladores com a lógica principal do jogo.
