# Captura de elementos utilizando Selenium

### Estratégias

- By.id - Localiza um elemento pelo atributo id.
- By.name - Localiza um elemento pelo atributo name.
- By.tagName - Localiza um elemento pela sua tag - Ex: input, span..
- By.linkText - Localiza o elemento pelo texto visível na tela do link - Geralmente utilizando quando ao passar o mouse pelo elemento o ícone é igual a imagem: ![](https://cdn3.iconfinder.com/data/icons/edition/100/hand_curser_rounded-16.png) 
- By.partialLinkText - Localiza o elemento pelo texto visível na tela parcial do link.
- By.className - Localiza o elemento pelo atributo class - Geralmente utilizado quando precisa-se capturar um elemento que tenha uma class exclusiva para ele,  e este possui mais classes no elemento:

```html
<button class="btn btn-principal btn-home">...</button>`
```

 Podemos localizar o button acima utilizando:

```java
By.className("btn-principal")
```

- By.cssSelector - Documentação abaixo.
- By.Xpath - Documentação abaixo.


# CSSSelector

- .class - Localiza o elemento atravez do conjunto do css removendo os espaços e adicionando pontos.

```java
By.cssSelector(".btn.btn-principal.btn-home")
```

- \#id - Localiza o elemento através do id.

```java
By.cssSelector("#btnPrincipal")
```

- Tag - Localiza o elemento atraves da tag - Ex: input, button, h3
- Elementos filho - Localiza o próximo elemento

```java
By.cssSelector("div > p")
```

#### Atributos
- Atributo igual

```java
By.cssSelector("div[style='background-color:#668CD9']")
```

- Atributo que inicia com determinado valor

```java
By.cssSelector("a[id^='splitbutton']")
```

- Atributo que termina com determinado valor

```java
By.cssSelector("input[name$='-ciss']")
```

- Atributo que contém um determinado valor

```java
By.cssSelector("div[class*='x-toolbar-manter']")
```


# Xpath

- //tag - Localiza pega tag

```java
By.xpath("//input")
```

- //tag[@atributo] - Localiza através de um atributo

```java
By.xpath("//input[@placeholder]")
```
- //tag[@atributo="valor"] - Localiza através do valor de um atributo

```java
By.xpath("//input[@class='old']")
```

- Elemento filho - Localiza o próximo elemento
		
```java
By.xpath("//div/ul/li/a")
By.xpath("//h4/span")
```
- Elemento pai - Localiza o elemento pai
		
```java
By.xpath("//h4/..")
```
- Elemento avô - Localiza o elemento avô
		
```java
By.xpath("//h4/../..")
```
- Elemento pela sua posição - Localiza um elemente de acordo com sua posição, é utilizado quando precisa capturar um elemento que tenha um ou mais com as mesmas tags
		
```java
By.xpath("//table/tbody/tr/td[4]")
```

#### Atributos
- Atributo que inicia
		
```java
By.xpath("//td[starts-with(@data-columnid,'ciss-primarykey')]")
```

- Atributo que contém o valor
		
```java
By.xpath("//input[contains(@id, 'senha')]"))
```

- Texto que contém o valor
		
```java
By.xpath("//button[contains(text(), 'Sair')]"))
```

- Texto que o texto é igual

```java
By.xpath("//button[.='Sair']")
```
