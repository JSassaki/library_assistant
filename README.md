# Assistente de biblioteca
**Autor:** Jorge Sassaki | [Linkedin](www.linkedin.com/in/jsassaki) | [Github](https://github.com/JSassaki)

O **objetivo** deste projeto é simples, **ajudar a recomendar livros para estudantes** baseado na entrada de um título de livro.

O assistente identifica o livro e retorna o nome do autor, só por sanity check. Caso o nome do autor esteja errado, pode ser que o modelo esteja alucinando ou que tenha confundido o livro!

Em seguida, dá a faixa etária mínima recomendada para o livro. Após isso, recomenda livros para diferentes faixas etárias que os estudantes podem ter. Isso serve para duas coisas:
1.   Caso o estudante seja mais jovem que o recomendado, provê alternativas adequadas à faixa etária do estudante;
2.   Caso o estudante tenha gostado de um livro e queira outros similares, provê alternativas também alternativas para ele.

Este projetinho foi inspirado pela necessidade real de uma amiga bibliotecária, que sempre fica na dúvida se alguma obra é adequada para a idade dos estudantes curiosos.

**To-dos:**
*   **Evitar que o modelo retorne o mesmo livro múltiplas vezes.** Por vezes, o modelo repete o livro em línguas diferentes, ou recomenda o mesmo livro para duas faixas etárias.
*   **Adicionar mais controles para a consulta.** No momento, a única entrada é o título do livro. Quero adicionar mais opções como gêneros, movimento literário, para filtrar melhor as recomendações.
*   **Melhorias de interface.**

**Problemas conhecidos:**
*    O retorno do gemini pode vir com "*finish_reason:* 5", sem resultado.
*    O modelo tem tendência a recomendar livros com uma temática similar, mas sem levar em conta os outros temas do livro. 
   *   Por exemplo: Heartstopper, um livro sobre romance adolescente, que trata temas como família e identidade. Um dos livros recomendados foi Anne Frank, não está completamente errado, mas a "vibe" é completamente diferente.
*   Para idades menores, o modelo parece ter um viés em recomendar Ziraldo e O Pequeno Príncipe. São excelentes recomendações, mas fica repetitivo.
*   Por algum motivo, a integração com o gradio só parece funcionar se estiver em modo debug.
