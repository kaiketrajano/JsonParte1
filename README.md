# JsonParte1
# Atividade 2 - Manipulação de String e Json - Parte 1

# O que é o Json e por que ele se tornou tão popular?

O Json é um formato leve e baseado em texto que é usado para representar dados estruturados, e sua popularidade 
se deve a sua usuablidade e compreensão simples de uso além de gerar e interpretar em varias linguaguens e sem muito utilizado em APIs e comunicação
entre cliente e servidor.

```js
        {
          "nome": "Kaike",
          "idade": 18,
          "curso": "Tecnologia em Sistemas para Internet"
        }
```

# Qual a diferença fundamental entre JSON.stringify() e JSON.parse()? Dê um
exemplo prático de quando usar cada um.

 - JSON.stringify(): transforma um objeto JavaScript em uma representação de texto no formato JSON.
 - JSON.parse(): faz o processo inverso: ele lê uma string em formato JSON e converte novamente em um objeto JavaScript utilizável.

```js

      const pessoa = { nome: "Kaike", idade: 18 };

      // transforma o objeto para texto JSON
      const json = JSON.stringify(pessoa);
      console.log(json); // {"nome":"Kaike","idade":18}
      
      // Converte o texto JSON de volta para objeto
      const obj = JSON.parse(json);
      console.log(obj.nome); //  Kaike


```
# Considerando a string "JavaScript é baseada em ECMA Script", quais métodos você usaria para:
  - Verificar se contém a palavra "Script";
  - Remover a palavra "JavaScript" e gerar uma nova string;
  - Substituir "baseada" por "tem origem"

a) Verificar se contém a palavra "Script":
```js
    const frase = "JavaScript é baseada em ECMA Script";
    console.log(frase.includes("Script")); // true
```
b) Remover a palavra "JavaScript" e gerar uma nova string:
```js
    const nova = frase.replace("JavaScript", "").trim();
    console.log(nova); // "é baseada em ECMA Script"
```
c) Substituir "baseada" por "tem origem":
```js
    const substituida = frase.replace("baseada", "tem origem");
    console.log(substituida); // "JavaScript é tem origem em ECMA Script"
```
# Qual a vantagem de usar template strings (``) em vez de concatenação com +
para criar strings complexas?

As template strings tornam o código mais limpo e fácil de ler, permitindo inserir variáveis diretamente dentro da string com ${} e escrever textos com várias linhas sem precisar usar \n.

- Exemplo com concatenação:
```js
      const linguagem = "JavaScript";
      const versao = 2025;
      console.log("A linguagem " + linguagem + " está atualizada para " + versao + ".");
```
- Exemplo com template string:
```js
      const linguagem = "JavaScript";
      const versao = 2025;
      console.log(`A linguagem ${linguagem} está atualizada para ${versao}.`);]
```
