---
description: ICE31 valida los estilos de fuente predefinidos que se usan en los controles que muestran texto. También valida que la propiedad DefaultUIFont hace referencia a un estilo de fuente válido.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277548"
---
# <a name="ice31"></a>ICE31

ICE31 valida los estilos de fuente predefinidos que se usan en [los controles](controls.md) que muestran texto. También valida que la propiedad [**DefaultUIFont**](defaultuifont.md) hace referencia a un estilo de fuente válido.

Los controles pueden tener un estilo de fuente predefinido, tal y como se describe en [Agregar controles y texto](adding-controls-and-text.md). Para establecer la fuente y el estilo de fuente de una cadena de texto, anteponga a la cadena de caracteres mostrados el prefijo { \\ style} o {&*Style*}. Donde Style es un identificador que aparece en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la propiedad [**DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente.

ICE31 comprueba la columna de texto de cada control de la [tabla de control](control-table.md) para comprobar que existe una entrada válida en la [tabla TextStyle](textstyle-table.md).

ICE31 omite el [control ScrollableText](scrollabletext-control.md).

## <a name="results"></a>Results

ICE31 expone un mensaje de error para estilos no definidos, nombres de estilo que son demasiado largos, una tabla de TextStyle que falta y etiquetas de estilo sin llave de cierre.

ICE31 expone una advertencia si la etiqueta de estilo no está al principio de la línea o si un control tiene varias etiquetas de estilo.

## <a name="example"></a>Ejemplo

ICE31 expone los siguientes errores para el ejemplo mostrado:

-   El control DialogB. Control1 usa BadStyle de TextStyle sin definir.
-   El control DialogB. Control2 usa BadStyle de TextStyle sin definir.
-   El control DialogB. Control6 no tiene llave de cierre en el estilo de texto.
-   El control DialogB. Control3 especifica un estilo de texto que es demasiado largo para ser válido.

ICE31 envía la siguiente advertencia para el ejemplo mostrado:

-   La etiqueta de estilo de texto de DialogB. Control4 no tiene ningún efecto. ¿Realmente desea que aparezca como texto?

[Tabla de control](control-table.md) (parcial)



| Diálogo  | Control  | Texto                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cuadro de diálogo | Control0 | { \\ OKStyle} este es el texto que se va a mostrar.                                                                                                                             |
| Cuadro de diálogo | Control1 | {&OKStyle} Este es el texto que se va a mostrar.                                                                                                                              |
| DialogB | Control1 | {&BadStyle} Este es el texto que se va a mostrar.                                                                                                                             |
| DialogB | Control2 | { \\ BadStyle} este es el texto que se va a mostrar.                                                                                                                            |
| DialogB | Control3 | {&estilo que está por encima de 72 caracteres y, por lo tanto, no puede ser un estilo aunque de algún modo se hubiera administrado para obtenerlo en la tabla de TextStyle} Este es el texto que se va a mostrar. |
| DialogB | Control4 | ADVERTENCIA { \\ OKStyle} este es el texto que se va a mostrar.                                                                                                                     |
| DialogB | Control5 | { \\ OKStyle} {&OKStyle} este es el texto que se va a mostrar.                                                                                                                   |
| DialogB | Control6 | { \\ OKStyle es el texto que se va a mostrar.                                                                                                                             |



 

[Tabla TextStyle](textstyle-table.md) (parcial)



| Estilo] |
|-----------|
| OkStyle   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



