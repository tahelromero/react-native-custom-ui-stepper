# react-native-custom-ui-stepper.

[![npm version](https://img.shields.io/npm/v/react-native-custom-ui-stepper.svg)](https://www.npmjs.com/package/react-native-custom-ui-stepper)
[![npm version](https://img.shields.io/npm/dt/react-native-custom-ui-stepper.svg)](https://img.shields.io/npm/dt/react-native-custom-ui-stepper.svg)

![Examples](https://i.imgur.com/D7OdHoh.png "Examples")


Un componente de React Native que refleja la funcionalidad de [UIStepper](https://developer.apple.com/reference/uikit/uistepper) de iOS.

> Un control de stepper proporciona una interfaz de usuario para incrementar o decrementar un valor. Un stepper muestra dos botones: uno con un símbolo de menos (“–”) y otro con un símbolo de más (“+”).

**Ahora puedes configurar tu react-native-custom-ui-stepper para que sea vertical**

## Instalación

`npm i react-native-custom-ui-stepper`

## Utilización

```javascript
import UIStepper from 'react-native-custom-ui-stepper';
...
setValue = (value) => {
  // do something with value
}
render() {
  return (
      <UIStepper
        onValueChange={(value) => { this.setValue(value) }}
      />
  )
}
```
Ahora puedes usar imágenes personalizadas, ya sea desde tu sistema de archivos local o desde Internet. Consulta [Props](#props) para más detalles.


## Demo

![Demo example](http://g.recordit.co/ipvGlYfRpa.gif "Demo example")

## Props

| Nombre                    | Tipo             | Descripción                                                                                                                                                                         | Valor por defecto                           |
| ----------------------- | ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- |
| `initialValue`          | Number           | Valor inicial                                                                                                                                                                         | 0                                 |
| `value`                 | Number           | Sobrescribir forzosamente el valor                                                                                                                                                         | 0                                 |
| `minimumValue`          | Number           | Valor mínimo                                                                                                                                                                       | 0                                 |
| `maximumValue`          | Number           | Valor máximo                                                                                                                                                                       | 100                               |
| `steps`                 | Number           | Valor de incremento                                                                                                                                                                     | 1                                 |
| `displayValue`          | Boolean          | Muestra el valor del stepper entre el botón de incremento y el de decremento                                                                                                               | false                             |
| `incrementImage`        | String or Number | Sobrescribir la imagen de incremento predeterminada                                                                                                                                                | require('./assets/increment.png') |
| `decrementImage`        | String or Number | Sobrescribir la imagen de decremento predeterminada                                                                                                                                                | require('./assets/decrement.png') |
| `wraps`                 | Boolean          | Cuando se establece en verdadero, incrementar más allá del `maximumValue` establecerá el valor en `minimumValue` y viceversa                                                                        | false                             |
| `tintColor`             | String           | Cambia el color de todos los píxeles no transparentes al tintColor                                                                                                               | #0076FF                           |
| `overrideTintColor`     | Boolean          | Al usar una imagen externa, establece si deseas que el tintColor se aplique a los píxeles no transparentes.                                                                           | false                             |
| `backgroundColor`       | String           | Color de fondo                                                                                                                                                                    | transparent                       |
| `vertical`              | Boolean          | Muestra un UI Stepper vertical. **Debes** especificar una altura y un ancho.                                                                                                           | false                             |
| `displayDecrementFirst` | Boolean          | Muestra el botón de decremento encima del botón de incremento, solo funciona cuando `vertical` es `true`                                                                                       | false                             |
| `width`                 | Number           | Ancho                                                                                                                                                                               | 94                                |
| `height`                | Number           | Alto                                                                                                                                                                              | 29                                |
| `textColor`             | String           | El color de texto deseado que se usará cuando `displayValue` esté configurado como `true`                                                                                                     | #0076FF                           |
| `fontFamily`            | String           | La familia de fuente utilizada en el valor mostrado cuando `displayValu`e esté configurado como `true`                                                                                                    | System                            |
| `fontSize`              | Number           | El tamaño de fuente utilizado en el valor mostrado cuando `displayValue` esté configurado como `true`                                                                                                      | 15                                |
| `borderColor`           | String           | Color utilizado para el borde                                                                                                                                                           | #0076FF                           |
| `borderWidth`           | Number           | Ancho del borde                                                                                                                                                                 | 1                                 |
| `borderRadius`          | Number           | Radio del borde                                                                                                                                                                | 4                                 |
| `onValueChange`         | Function         | Ejecutada cuando el valor cambia. El valor se pasa como parámetro                                                                                                                | null                              |
| `onIncrement`           | Function         | Ejecutada cuando el usuario hace clic en el botón de incremento (+). El valor se pasa como parámetro                                                                                          | null                              |
| `onDecrement`           | Function         | Ejecutada cuando el usuario hace clic en el botón de decremento (–). El valor se pasa como parámetro                                                                                          | null                              |
| `onMinimumReached`      | Function         | Ejecutada cuando se alcanza el `minimumValue`. El valor se pasa como parámetro                                                                                                     | null                              |
| `onMaximumReached`      | Function         | Ejecutada cuando se alcanza el `maximumValue`. El valor se pasa como parámetro                                                                                                     | null                              |
| `innerRef`              | Function         | Una referencia al UIStepper renderizado. Puedes usar esto para acceder a métodos basados en clases. `increment()`, `decrement()`, `resetValue()` y `setValue()` son los más comunes | null                              |

## Contribuciones

No hay requisitos para contribuir al paquete react-native-custom-ui-stepper. Puedes [Navegar a](https://github.com/tahelromero/react-native-custom-ui-stepper/issues/) o plantear problemas en los que te gustaría contribuir.

Haz un fork del repositorio en Github
Clona el proyecto
Realiza cambios y súbelos a tu rama forkeada
Envía tus cambios a tu rama
Envía un Pull Request para que se pueda fusionar en react-native-custom-ui-stepper

## Ejecutar ejemplo

```
$ git clone https://github.com/tahelromero/react-native-custom-ui-stepper.git
$ cd example
$ yarn # or npm install
$ react-native run-ios
```
