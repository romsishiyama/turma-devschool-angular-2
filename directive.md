
# Aula de Diretivas Angular!

Para a essas aula vamos abordar os seguintes tópicos:
- O Que São Diretivas;
- Component Directives;
- Structural Directives;
- Attribute Directives;
- Como Criar Uma Diretiva Personalizada;
- Exercícios de fixação;

# O Que São Diretivas

As directives (diretivas) em Angular são uma classe js, declarada como @directive. Temos 3 diretivas em Angular; estão listadas abaixo:

## Component Directives

Eles formam a classe principal, com detalhes de como o componente deve ser processado, instanciado e usado em tempo de execução.

## Structural Directives

Uma diretiva de estrutura lida basicamente com a manipulação dos elementos dom. As diretivas estruturais têm um sinal * antes da diretiva. Por exemplo, **ngIf** e **ngFor** .

## Attribute Directives

As diretivas de atributo tratam de alterar a aparência e o comportamento do elemento dom. Você pode criar suas próprias diretivas, conforme explicado na seção abaixo.

# Como Criar Uma Diretiva Personalizada?
Podemos criar uma diretiva personalizada utilizando o comando **ng g directive shared/directives/blue** onde **ng g directive** é o comando do client do angular para gerar a diretiva e **shared/directives** é o local da pasta e **blue** é o nome da nossa diretiva. Esse é um exemplo da saída do console:

![enter image description here](https://github.com/NathanCarlos/turma-devschool/blob/main/imagens-ilustrativas/diretivas/exemplo-saida-console-diretiva.PNG?raw=true)

Esses dois arquivos serão gerados:

![enter image description here](https://github.com/NathanCarlos/turma-devschool/blob/main/imagens-ilustrativas/diretivas/exemplo-arquivos-gerados-diretivas.PNG?raw=true)

Nos parâmetros do construtor da nossa diretiva, precisamos colocar uma referência ao elemento que será utilizado pela diretiva colocando esse código abaixo:
>private  element: ElementRef

e também precisamos colocar dentro do construtor o bloco de código abaixo:
>element.nativeElement.style.color = 'blue';

No final o nosso arquivo da diretiva deverá ficar assim:
![enter image description here](https://github.com/NathanCarlos/turma-devschool/blob/main/imagens-ilustrativas/diretivas/exemplo-arquivo-diretiva-constructor.PNG?raw=true)

Agora que já geramos os arquivos e também ajustamos nossa diretiva para alterar o comportamento do elemento que utiliza-la, só falta colocar em alguma tag html o seletor da nossa diretiva para ela ser utilizada, como no exemplo abaixo:

![enter image description here](https://github.com/NathanCarlos/turma-devschool/blob/main/imagens-ilustrativas/diretivas/exemplo-diretiva-blue-no-elemento.PNG?raw=true)

Esse será o resultado final ao rodar o seu projeto:

![enter image description here](https://github.com/NathanCarlos/turma-devschool/blob/main/imagens-ilustrativas/diretivas/exemplo-saida-final.PNG?raw=true)

No meu caso, coloquei no meu h3 do header.component, então ele atualizou o texto para ficar em azul.

## Lista de exercícios
Para conseguir realizar a lista de exercícios aguarde a aula para um entendimento melhor, porém se quiser se desafiar a fazer tudo bem :)

Exercício 1) Crie uma diretiva de atributo para alterar a cor de elementos quando for utilizada.

Exercício 2) Para esse exercício, utilize o projeto de tarefas criado na lista de exercícios desse link: https://github.com/NathanCarlos/turma-devschool/blob/main/event-binding-simples.md e na listagem das tarefas coloque um ngIf para quando não tiver tarefas com base na busca, exibir a seguinte mensagem: "Não existe tarefas para essa busca!".

Exercício 3) Utilize ngClass para estilizar a tarefa completa/incompleta de formas diferentes.
