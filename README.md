# canvas-desenhe-com-mouse
Um exemplo simples de desenho com o mouse usando o elemento Canvas em HTML

<script>
    // Função para desenhar um quadrado na posição (x, y) com determinado tamanho e cor
    function desenhaQuadrado(x, y, tamanho, cor) 
    

    // Função para desenhar um círculo na posição (x, y) com determinado raio e cor
    function desenhaCirculo(x, y, raio, cor) 
    
 
    // Função para desenhar a paleta de cores (quadrados vermelho, verde e azul)
    function desenhaPaletaDeCores()
    
    
    // Função para lidar com o movimento do mouse
    function lidaComMovimentoDoMouse(evento) 
    
    
        // Verifica se o desenho está habilitado (variável desenha é verdadeira) e se é possível desenhar na área específica
        if (desenha && podeDesenharNaArea(x, y)) {
           
    
    // Função para habilitar o desenho
    function habilitaDesenhar()
    
    // Função para desabilitar o desenho
    function desabilitaDesenhar()
   
    // Função para verificar se é possível desenhar na área específica
    function podeDesenharNaArea(x, y) 
    
    // Função para selecionar a cor com base na posição do clique do mouse
    function selecionaCor(evento) 
    
    
        // Cada condição altera a variável corAtual com base na posição do clique
        // A posição y é a mesma em todos os casos
        if (y > yQuadrados && y < yQuadrados + tamanhoQuadrados) {
            if (x > xVermelho && x < xVermelho + tamanhoQuadrados) {
                corAtual = 'red'; // Define a cor atual como vermelho
            }
