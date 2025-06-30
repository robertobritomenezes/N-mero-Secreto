# 🎯 Jogo de Adivinhação - Número Secreto

Bem-vindo ao **Jogo de Adivinhação**!  
Este é um projeto simples feito em JavaScript onde o jogador deve adivinhar um número secreto entre 1 e 100.

## 💡 Como funciona?

- Ao iniciar o jogo, um número secreto é gerado aleatoriamente entre 1 e 100.
- O jogador deve digitar palpites até acertar o número.
- A cada tentativa, o jogo informa se o número secreto é **maior** ou **menor** que o chute.
- No final, o jogador recebe uma mensagem de parabéns com o número de tentativas usadas.

## 🛠️ Tecnologias Utilizadas

- HTML (para estrutura da página, opcional)
- JavaScript (lógica principal do jogo)
- `alert()` e `prompt()` para interação com o usuário

## 📂 Como executar

1. Copie o código para um arquivo `.html`:
    ```html
    <!DOCTYPE html>
    <html lang="pt-BR">
    <head>
        <meta charset="UTF-8">
        <title>Jogo de Adivinhação</title>
    </head>
    <body>
        <script>
            alert("Seja Bem-vindo ao Jogo");

            let numeroSecreto = parseInt(Math.random() * 100 + 1);
            console.log(numeroSecreto);  // apenas para debug

            let chute;
            let tentativas = 1;

            while (chute != numeroSecreto) {
                chute = prompt("Escolha um número entre 1 a 100");

                if (chute == numeroSecreto) {
                    break;
                } else {
                    if (chute > numeroSecreto) {
                        alert(`O número secreto é menor que ${chute}`);
                    } else {
                        alert(`O número secreto é maior que ${chute}`);
                    }
                    tentativas++;
                }
            }

            let palavraTentativa = tentativas > 1 ? "tentativas" : "tentativa";
            alert(`Parabéns! Você descobriu o número secreto ${numeroSecreto} com ${tentativas} ${palavraTentativa}.`);
        </script>
    </body>
    </html>
    ```

2. Salve o arquivo com a extensão `.html`, por exemplo: `jogo.html`.
3. Abra o arquivo em um navegador moderno (Chrome, Firefox, etc.).
4. Jogue! 🎉

## ✅ Melhorias Futuras (Ideias)

- Limite de tentativas
- Histórico dos palpites anteriores
- Interface com HTML e CSS estilizados
- Botão "Jogar novamente"
- Versão com pontuação
