# js_utilidade
Utilidades para js

## Remover acentos e caracteres especiais (firefox | ie | chrome)
```javascript
function sem_acento(event) {
  if (document.all){
    var evt	= event.keyCode;
  }else{
    var evt = event.charCode;
  }
  var valid_chars = '0123456789abcdefghijlmnopqrstuvxzwykABCDEFGHIJLMNOPQRSTUVXZWYK';
  var chr= String.fromCharCode(evt);
  if (valid_chars.indexOf(chr)>-1 ){return true;}
  if (valid_chars.indexOf(chr)>-1 || evt < 9 || evt == 32){return true;}
  return false;
}

$('input').on('keypress', function(event){ 
  return sem_acento(event);
});
```

## Mascara
https://igorescobar.github.io/jQuery-Mask-Plugin/

## Logic-less templates
https://mustache.github.io/
