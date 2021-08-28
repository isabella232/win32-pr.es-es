---
description: ICE31 valida los estilos de fuente predefinidos que se usan en los controles que muestran texto. También valida que la propiedad DefaultUIFont hace referencia a un estilo de fuente válido.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 783c8b842f80707bbd1ca833fbc7ad1f154a47a0d3aa24377ee58a1c6549bf7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528675"
---
# <a name="ice31"></a>ICE31

ICE31 valida los estilos de fuente predefinidos que se usan en [los controles que](controls.md) muestran texto. También valida que la [**propiedad DefaultUIFont**](defaultuifont.md) hace referencia a un estilo de fuente válido.

Los controles pueden tener un estilo de fuente predefinido como se describe [en Agregar controles y texto.](adding-controls-and-text.md) Para establecer la fuente y el estilo de fuente de una cadena de texto, antefirima la cadena de caracteres mostrados con { style} o \\ {&*style*}. Donde style es un identificador enumerado en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la [**propiedad DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente.

ICE31 comprueba la columna Texto de cada control de la [tabla de controles](control-table.md) para comprobar que existe una entrada válida en la tabla [TextStyle](textstyle-table.md).

ICE31 omite el control [ScrollableText](scrollabletext-control.md).

## <a name="results"></a>Results

ICE31 publica un mensaje de error para estilos no definidos, nombres de estilo demasiado largos, una tabla TextStyle que falta y etiquetas de estilo sin llave de cierre.

ICE31 envía una advertencia si la etiqueta de estilo no está al principio de la línea o si un control tiene varias etiquetas de estilo.

## <a name="example"></a>Ejemplo

ICE31 publica los siguientes errores para el ejemplo que se muestra:

-   El control DialogB.Control1 usa Undefined TextStyle BadStyle.
-   El control DialogB.Control2 usa Undefined TextStyle BadStyle.
-   Al control DialogB.Control6 le falta la llave de cierre en el estilo de texto.
-   Control DialogB.Control3 especifica un estilo de texto que es demasiado largo para ser válido.

ICE31 publica la siguiente advertencia para el ejemplo que se muestra:

-   La etiqueta Estilo de texto en DialogB.Control4 no tiene ningún efecto. ¿Realmente quiere que aparezca como texto?

[Tabla de control](control-table.md) (parcial)



| Diálogo  | Control  | Texto                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DialogA | Control0 | { \\ OKStyle}Este es el texto que se va a mostrar.                                                                                                                             |
| DialogA | Control1 | {&OKStyle} Este es el texto que se va a mostrar.                                                                                                                              |
| DialogB | Control1 | {&BadStyle} Este es el texto que se va a mostrar.                                                                                                                             |
| DialogB | Control2 | { \\ BadStyle}Este es el texto que se va a mostrar.                                                                                                                            |
| DialogB | Control3 | {&que tiene más de 72 caracteres y, por lo tanto, no puede ser posiblemente un estilo aunque de algún modo lo lograra obtener en la tabla TextStyle} Este es el texto que se va a mostrar. |
| DialogB | Control4 | Advertencia { \\ OKStyle}Este es el texto que se va a mostrar.                                                                                                                     |
| DialogB | Control5 | { \\ OKStyle}{&OKStyle}Este es el texto que se va a mostrar.                                                                                                                   |
| DialogB | Control6 | { \\ OKStyle Este es el texto que se va a mostrar.                                                                                                                             |



 

[Tabla TextStyle](textstyle-table.md) (parcial)



| Textstyle |
|-----------|
| OkStyle   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



