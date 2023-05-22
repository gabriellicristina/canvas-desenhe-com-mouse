# canvas-desenhe-com-mouse
Um exemplo simples de desenho com o mouse usando o elemento Canvas em HTML
<meta charset="UTF-8">

<canvas width="600" height="400"></canvas>

<script>
    // Função para desenhar um quadrado na posição (x, y) com determinado tamanho e cor
    function desenhaQuadrado(x, y, tamanho, cor) {
        pincel.fillStyle = cor;
        pincel.fillRect(x, y, tamanho, tamanho)
        pincel.fill();
    }

    // Função para desenhar um círculo na posição (x, y) com determinado raio e cor
    function desenhaCirculo(x, y, raio, cor) {
        pincel.fillStyle = cor; // o padrão é azul (blue)
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * 3.14);
        pincel.fill();
    }

    // Função para desenhar a paleta de cores (quadrados vermelho, verde e azul)
    function desenhaPaletaDeCores() {
        desenhaQuadrado(xVermelho, yQuadrados, tamanhoQuadrados, 'red');
        desenhaQuadrado(xVerde, yQuadrados, tamanhoQuadrados, 'green');
        desenhaQuadrado(xAzul, yQuadrados, tamanhoQuadrados, 'blue');
    }

    // Função para lidar com o movimento do mouse
    function lidaComMovimentoDoMouse(evento) {
        var x = evento.pageX - tela.offsetLeft;
        var y = evento.pageY - tela.offsetTop;

        // Verifica se o desenho está habilitado (variável desenha é verdadeira) e se é possível desenhar na área específica
        if (desenha && podeDesenharNaArea(x, y)) {
            desenhaCirculo(x, y, 5, corAtual); // Desenha um círculo na posição atual com raio 5 e cor corAtual
        }
    }

    // Função para habilitar o desenho
    function habilitaDesenhar() {
        desenha = true;
    }

    // Função para desabilitar o desenho
    function desabilitaDesenhar() {
        desenha = false;
    }

    // Função para verificar se é possível desenhar na área específica
    function podeDesenharNaArea(x, y) {
        if (x >= 0 && x < 3 * tamanhoQuadrados && y >= 0 && y < tamanhoQuadrados) {
            return false;
        } else {
            return true;
        }
    }

    // Função para selecionar a cor com base na posição do clique do mouse
    function selecionaCor(evento) {
        var x = evento.pageX - tela.offsetLeft;
        var y = evento.pageY - tela.offsetTop;

        // Cada condição altera a variável corAtual com base na posição do clique
        // A posição y é a mesma em todos os casos
        if (y > yQuadrados && y < yQuadrados + tamanhoQuadrados) {
            if (x > xVermelho && x < xVermelho + tamanhoQuadrados) {
                corAtual = 'red'; // Define a cor atual como vermelho
            }
