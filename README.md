# Fractais em Haskell!!! :star_struck: :star_struck: :star_struck:

## O que são fractais? :thinking:	

São figuras geométricas, produzidas por meio de equações matemáticas que podem ser interpretadas como formas e cores por programas de computador. O fractal pode ser dividido em partes, sendo cada uma delas semelhantes ao objeto original e com infinitos detalhes. Na maioria dos casos, um fractal pode ser gerado por um padrão repetido, normalmente por processos iterativos. Se você der um zoom em um fractal, ele revelara novos detalhes. :open_mouth:	

Exemplo de um fractal de Mandelbrot sendo ampliado por mais de uma hora!!➡️➡️https://youtu.be/pCpLWbHVNhk

## Conjunto de Mandelbrot:

O conjunto de Mandelbrot é um fractal definido como o conjunto de pontos c no plano complexo para o qual a sequência é definida recursivamente, Benoit Mandelbrot foi o matemático que criou o termo fractal e teve grande contribuição na área de geometria fractal. 

## Vamos ao código...

### Gerador de fractal em Haskell:

Nos baseamos em dois programas para a execução do trabalho. Você pode acessar o código original através do link:

➡️ https://typeclasses.com/art/mandelbrot

➡️ https://gist.github.com/mbrc12/c3a40215022ea8efcddf7ad39993e4f3

O primeiro programa é mais simples e com mais limitações para a personalização de fractais e sua cor.

Código:⬇️⬇️

![IMG1](https://user-images.githubusercontent.com/93085789/176334678-e6b32822-ff16-4814-9908-bad6de55a32b.jpeg)

Funções principais⬇️

aspectRatio : define um número complexo <br/>
Width, height : resolução da imagem <br/>
maxIters : número de iterações do programa <br/>
fractal : equação que define o fractal <br/>
realize : gera as espirais <br/>

Executando o código, o fractal formado será:

![image](https://user-images.githubusercontent.com/93085789/176335333-9daaa435-fca6-41f0-ad16-1a2db3228768.png) <br/>
Um fractal bem simples.

O segundo programa se apresenta de forma mais clara e customizável, o que nos permitiu gerar diversos tipos de fractais. 

Código:⬇️⬇️
![1](https://user-images.githubusercontent.com/93085789/176339894-6dc9244e-5b83-44ac-8052-b7a540a33806.jpeg)
![2](https://user-images.githubusercontent.com/93085789/176339916-4cf2f800-f1bf-4592-af92-78a1b9bd631e.jpeg)
![3](https://user-images.githubusercontent.com/93085789/176339929-f892ad48-ac87-4850-8197-60259a425b65.jpeg)
![5](https://user-images.githubusercontent.com/93085789/176339958-400d812c-8b1d-4613-9bbc-70d9a711da4d.jpeg)
![6](https://user-images.githubusercontent.com/93085789/176339971-5b49154d-0ce0-48f6-b2d7-b852ef2c4d17.jpeg)
![7](https://user-images.githubusercontent.com/93085789/176339992-cc1f5c0f-18a5-4de1-bd03-22879237ad9f.jpeg)

Funções principais⬇️

characteristic : quando z fica maior que 2 a função estoura, então é feita uma função para que isso não ocorra, fazendo o valor inverso de quando estamos no "final" dos buracos <br/>
parser : colocar o valor das iterações e as principais variáveis para a formação da imagem <br/>
colorFunc : é a função de cor, x é a variável que muda as cores, w é o width e r, g e b são os RGBs normais <br/>  
produceFractal : define o tamanho e a largura da imagem, desenha os pixels e gera a função do desenho <br/>
clamp, normal sigmoidCut: definem a propriedade dos fractais <br/>

Executando o código, o fractal formado será:

Nesse exemplo, precisaremos ir um pouco mais a fundo no código.
Modificamos a função baseFunction⬇️⬇️ <br/>
![func](https://user-images.githubusercontent.com/93085789/176439831-1bbbfe17-24f5-47ce-b727-82bdb35e1e11.jpeg) <br/>
Mudaremos o número de iterações para 255⬇️⬇️ <br/>
![iter](https://user-images.githubusercontent.com/93085789/176440244-7f659bc5-7428-4242-ae4c-419cf45d5826.jpeg) <br/>
Alteramos a origem do x e y e as cores do fractal, gerando a imagem: <br/>

![IMG5](https://user-images.githubusercontent.com/93085789/176439210-c2802a22-68f1-47a4-a24d-a0a42e6ad355.jpeg) <br/>

Deixando em preto e branco ficaremos com uma imagem mais clara: <br/>

![IMG6](https://user-images.githubusercontent.com/93085789/176439273-1ba64521-8a39-4b35-b49a-c5f8af83fb09.jpeg) <br/>
Essa forma de mandelbrot⬆️ é chamada de burning ship, pois se parece com um navio pegando fogo.
