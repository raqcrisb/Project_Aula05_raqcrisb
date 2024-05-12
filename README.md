# Project_Aula05_raqcrisb

# Descrição do projeto

 Com base no perfil descrito pelo usuário, o sistema irá indicar o tipo de bike que melhor combina com o estilo deste usuário.

### Exemplo da execução:
" _Com base em seu perfil será indicado o tipo de bike que melhor combina com você_ ."
" _Descreva em poucas palavras como você é. Por exemplo, sou otimista_ ! "
**Se no prompt o usuário digitar** : 
" _Sou uma pessoa otimista, qual bike é melhor pra mim_ ?"
**A resposta será** :  
"_O modelo montain bike é o ideal para quem gosta da natureza, como pedalar por horas em montanhas ou campos abertos_ .."


### Sobre o sistema

  Utilizando o modelo *embedContent*, o sistema armazena em uma tabela o título e o conteúdo, sendo que o título é representado pelos seguintes perfis: aventureiro, acelerado, tranquilo ou acomodado.
| Título | Conteúdo | Embedding
| ------ | ------ | ------ |
| Aventureiro | O modelo montain bike é o ideal para quem gost...|	[-0.059365977, -0.067413956, -0.013067978, 0.0... |
| Acelerado |	O modelo speed é pra quem gosta de vento na ca... |	[0.016806815, -0.038365476, -0.01666913, 0.037... |
| Tranquilo |	O modelo urbano é para uma pessoa tranquila. E... |	[-0.007641607, -0.0577596, -0.031231815, 0.031... |
| Acomodado |	O modelo elétrico pode conter pedalada assisti...|	[-0.02872042, -0.02650506, -0.058923826, -0.00... |
  
  A resposta representada pelo conteúdo tem seu texto alterado a cada execução do prompt, devido a linha: f"Mude o texto a cada execução, sem adicionar informações que não façam parte do texto: {prompt}".
  

### Métodos utilizados

  _Método para trabalhar com o datasheet que insere o embedding em uma nova coluna_
  **def embed_fn(title, texto)** : 

  _Este método procura dentro desta lista de produtos escalares qual que tem a maior simularidade com a pergunta do usuário e obtém o ID dele_
  **def gerar_e_buscar_consulta(consulta, base, model)** :
   
### Autora:

   Raquel C. Bosnardo
 
