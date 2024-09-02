## Uso do Flexbox
### Por que usar Flexbox?
O Flexbox (ou "Flexible Box Layout") é uma tecnologia de layout no CSS que facilita a criação de layouts complexos e responsivos sem precisar recorrer a posicionamentos flutuantes (floats) ou tabelas. Ele é ideal para distribuir espaço entre os itens em um contêiner e controlar o alinhamento dos elementos em uma página, mesmo quando o tamanho dos elementos ou o espaço disponível varia.

## Flexbox do projeto "todo"
Neste projeto, o Flexbox foi utilizado principalmente para organizar os dias da semana e as tarefas associadas, garantindo que o layout seja flexível e se adapte ao tamanho da tela.
### Container principal (.container)
```CSS
.container {
    border: 2px solid snow;
    display: flex;
}
```
- **display: flex;** Este é o ponto de partida para ativar o comportamento flexível dentro do contêiner .container. Com isso, todos os elementos filhos desse contêiner serão organizados em um layout flexível, alinhando-se conforme o espaço disponível.
### Organização em Colunas (.week)
```CSS
.week {
    display: inline-flex;
    flex-grow: 3;
    flex-direction: column;
}
```  
- **flex-direction: column;** Define que os itens dentro do contêiner .week serão dispostos em uma coluna. Isso significa que os dias da semana (e suas tarefas) serão organizados verticalmente, de cima para baixo.
- **flex-grow: 3;** Permite que o contêiner .week cresça proporcionalmente para ocupar mais espaço, se necessário. Neste caso, ele é definido para ocupar três vezes mais espaço comparado ao outro contêiner ao lado (o de lembretes).


### Distribuição dos Itens (.row)
```CSS
.row {
    min-height: 200px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    align-items: center;
}
```
- **display: flex;** Ativa o Flexbox para o contêiner .row, onde cada linha representa um dia da semana com suas respectivas tarefas.
- **flex-wrap: wrap;** Permite que os itens se movam para a próxima linha se o espaço horizontal não for suficiente, o que é útil em layouts responsivos.
- **justify-content** space-around;: Distribui os itens igualmente com espaços ao redor deles, garantindo que haja um espaço uniforme entre os dias e as tarefas, além de margens externas consistentes
- **align-items** center;: Alinha verticalmente os itens no centro do contêiner .row, garantindo que todos os elementos estejam centrados na linha.
## Vantagens de Usar Flexbox
- **Flexibilidade**: Permite criar layouts que se ajustam automaticamente a diferentes tamanhos de tela e mudanças dinâmicas no conteúdo.
- **Simplicidade**: Reduz a complexidade do código CSS, eliminando a necessidade de hacks ou cálculos manuais para alinhar elementos.
- **Responsividade**: Facilita a criação de layouts que funcionam bem em dispositivos móveis, tablets e desktops sem a necessidade de media queries complexas.
