# Javascript VS jQuery

Um assunto muito abordado em grupos é `Javascript` ou `jQuery`?
<img src="https://image.slidesharecdn.com/domselectingjquery-140418230942-phpapp01/95/dom-selecting-jquery-42-638.jpg?cb=1397862678">
> Acredito que essa imagem fale por sí, certo?
Então vamos ao que importa, que é mostrar que certas coisas podem e devem ser usadas sem o `jQuery`, hoje em dia muitas pessoas não sabem nem o **_basico_** de `JavaScript`.

Vamos começar com os **SELETORES**

```
// No velho JS
document.getElementById('myId')
```
```
// Com jQuery
$('#myId')
```
Caso sejá uma `class`
```
// Javascript
document.querySelectorAll('myClass')

// Javascript "RAPIDO"
document.getElementsByClassName('myClass')

// jQuery
$('.myClass')
```
Manipulando o **DOM**
```
// jQuery
$('#myDiv').append('<img src="">')

// Javascript (FORMA RUIM)
document.getElementById('myDiv').innerHTML +=  '<img src="">'

// Javascript (FORMA MELHOR)
let fragment = document.createDocumentFragment()

let img = document.createElement('IMG')
img.src = ''

img.appendChild(fragment)
```


E se formos para um lado um pouco diferente? que tal mostrar e ocultar uma `div`.
```
// Ocultamos
document.getElementById('myId').style.display = 'none'

// Exibimos
document.getElementById('myId').style.display = 'block'
```

```
// Ocultamos
$('#myId').hide()

// Exibimos
$('#myId').show()
```

> Não vai cair a mão, certo?

Que tal, um pouco do famoso `click`?

```
let div = document.getElementById('myDiv')

div.onclick = () => {
  alert('Cliquei ;)')
}
```

```
$('#myDiv').on('click', function(){
  alert('Cliquei :/')
})
```

> Nem tudo é tão dificil como você costumava pensar...

Vamos trabalhar com a soma do `IMC`
```
function calcularImc(peso, altura){
  let imc = peso / (altura * altura)
  
  return imc
}

document.getElementById('myDiv').innerHTML += ' ' + calcularImcC(80, 171)
```

```
function calcularImc(peso, altura){
  var imc = peso / (altura * altura)
  
  return imc
}

$('#myId').append(calcularImcC(80, 171))
```
> Nem tem tanta diferença, certo?
