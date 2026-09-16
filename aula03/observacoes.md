# Observações sobre Elementos HTML (Block vs. Inline)

## Tabela de Elementos

| Elemento               | O que observar                                          | Block ou inline? | Explicação do comportamento                                                                                                                                  |
| :--------------------- | :------------------------------------------------------ | :--------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **h1, h2, h3**         | O destaque ocupa a linha inteira ou só o texto?         | Block            | Faz sentido ocuparem a linha inteira porque títulos principais estruturam a página em blocos verticais distintos, empurrando o conteúdo seguinte para baixo. |
| **p**                  | O destaque ocupa a linha inteira ou só o texto?         | Block            | Parágrafos representam blocos de texto independentes, portanto precisam quebrar a linha antes e depois para manter a leitura organizada.                     |
| **ul, ol**             | O destaque ocupa a linha inteira ou só a lista?         | Block            | Listas são estruturas de bloco vertical que contêm múltiplos itens, exigindo espaço próprio na página para não se misturarem com o texto corrido.            |
| **a (link no menu)**   | O destaque ocupa a linha inteira ou só o texto do link? | Inline           | O link serve para destacar uma palavra ou frase dentro de uma frase maior, sem interromper o fluxo horizontal do texto.                                      |
| **strong dentro de p** | O destaque ocupa a linha inteira ou só a palavra?       | Inline           | O modificador de ênfase (`strong`) altera apenas um trecho específico do texto, devendo fluir naturalmente dentro da linha.                                  |
| **img**                | O destaque ocupa a linha inteira ou só a imagem?        | Inline           | Por padrão, imagens comportam-se como elementos inline (ou inline-block), permitindo que fiquem alinhadas lado a lado com o texto.                           |

---

## Experimento: Comparação de Comportamentos

### 1. Dois elementos `<strong>` um do lado do outro no mesmo parágrafo

- **O que acontece:** Eles aparecem **na mesma linha**, lado a lado, sem quebra de linha entre eles.
- **Por quê:** Como o elemento `strong` é do tipo **inline**, ele ocupa apenas o espaço estritamente necessário para o seu conteúdo e flui junto com o texto vizinho.

### 2. Dois elementos `<p>` um do lado do outro no código

- **O que acontece:** O segundo parágrafo aparece obrigatoriamente **abaixo** do primeiro, ocupando linhas distintas.
- **Por quê:** Como o elemento `p` é do tipo **block**, ele força uma quebra de linha automática antes e depois de si, ocupando toda a largura disponível no container.
