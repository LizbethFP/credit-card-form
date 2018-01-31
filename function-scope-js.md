## Funciones globales: 1
##### La función ***$(document).ready(function() {}*** es una función anónima y global con respecto al contexto de ejecución de document, pero es una función local con respecto al contexto de ejecución window.

## Variables globales: 6
##### Las siguienes son variables globales en el contexto de ejecución de document, pero son variables locales para el contexto de ejecución global window:
* ***$inputCard***
* ***$inputMonth***
* ***$inputYear***
* ***$buttonNext***
* ***regexOnlyNumbers***
* ***labelErrorOrSuccessMessages***

## Funciones locales: 5
#### Las siguienes son funciones locales para el contexto de ejecución de la función anónima y global ***$(document).ready(function() {}***:
* ***function activeButton() {}***
* ***function desactiveButton() {}***
* ***function longitud(input) {}***
* ***function soloNumeros(input) {}***
* ***function isValidCreditCar(numberCard){}***

### Funciones callback: 1
#### La función parámetro ***longitud(numberCard)*** que es llamada de vuelta en la función ***function isValidCreditCard(numberCard)*** se ejecuta cuando esta útlima haya terminado de ejecutarse.

* function isValidCreditCard(numberCard) {
  var creditCardNumber = ***soloNumeros(longitud(numberCard))};***

### Function Expression: 0
#### Es una función que omite el nombre de la función para crear una función anónima que se asigna a una variable.

### Function statement: 5
#### Las siguientes son funciones declaradas que se guardan para usarse luego y que se ejecutarán luego cuando se les llame:
* ***function activeButton() {}***
* ***function desactiveButton() {}***
* ***function longitud(input) {}***
* ***function soloNumeros(input) {}***
* ***function isValidCreditCar(numberCard){}***

### Clousure: 0
#### Es una función que es libre de variables

### Scope: 3
#### Las siguientes funciones y ciclos son scopes cuyas varibles contenidas son variables locales, ya que solo son accesibles dentro de estos:
* $(document).ready(function() {
  ***var $inputCard = $('#card-number');***

  ***var $inputMonth = $('.input-month');***

  ***var $inputYear = $('.input-year');***

  ***var $buttonNext = $('#next');***

  ***var regexOnlyNumbers = /^[0-9]+$/;***

  ***var labelErrorOrSuccessMessages = $('label[for="card-number"]');***
};

* function soloNumeros(input) {
  ***var regex = /^[0-9]+$/;***
  if (regex.test(input)) {
    return input;
  }
}

* function isValidCreditCard(numberCard) {
  ***var creditCardNumber = soloNumeros(longitud(numberCard));***
  if (creditCardNumber !== undefined) {
    ***var arr = [];***
    ***var sumaTotal = 0;***
    for (***var index = creditCardNumber.length - 1***; index >= 0; index--) {
      arr.push(creditCardNumber[index]);
    }
    for (***var index = 1***; index < arr.length; index = index + 2) {
      arr[index] = arr[index] * 2;
      if (arr[index] >= 10) {
        arr[index] = arr[index] - 9;
      }
    }

    for (***var index = 0***; index < arr.length; index++) {
      sumaTotal = sumaTotal + parseInt(arr[index]);
    }

### Funciones que forman parte de la PILA: 5
* ***function activeButton() {}***
* ***function desactiveButton() {}***
* ***function longitud(input) {}***
* ***function soloNumeros(input) {}***
* ***function isValidCreditCar(numberCard){}***

### Funciones que forman parte de la COLA: 1
* ***$inputCard.on('input', function() {
    isValidCreditCard($(this).val().trim());
  });***
