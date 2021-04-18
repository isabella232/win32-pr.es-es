---
title: Agregar el BUTTONELEMENT de juego
description: Agregar el BUTTONELEMENT de juego
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- crear máscaras, elemento BUTTONELEMENT
- Aspectos de Windows Media Player, elemento BUTTONELEMENT
- máscaras, elemento BUTTONELEMENT
- archivos de definición de máscara, elemento BUTTONELEMENT
- BUTTONELEMENT (elemento)
- elementos, BUTTONELEMENT
- crear máscaras, reproducir botones
- Aspectos de Windows Media Player, botones de reproducción
- máscaras, botones de reproducción
- archivos de definición de máscara, botones de reproducción
- Reproducir botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532170"
---
# <a name="adding-the-play-buttonelement"></a>Agregar el BUTTONELEMENT de juego

Por último, puede Agregar los elementos **BUTTONELEMENT** que conectan los botones visuales de la pantalla a las acciones de Media Player de Windows. Este es el núcleo de la piel y puede imaginarse como el cableado de la superficie de la piel a la maquinaria interna de Windows Media Player.

Los **BUTTONELEMENT** s se encuentran dentro de un **BUTTONGROUP**. Siempre debe haber al menos un **BUTTONELEMENT** dentro de cada **BUTTONGROUP**.

Coloque el código **BUTTONELEMENT** de Play después del corchete angular de cierre de **BUTTONGROUP**.


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



Los atributos siguientes se usan para definir **BUTTONELEMENT** para el botón de reproducción:

**mappingColor**

Este es el valor de color de una región en el archivo de imagen de asignación que creó antes. En este caso, es el color verde sólido. Este atributo es necesario para cualquier **BUTTONELEMENT**. Al definir este color, está indicando a Windows Media Player que asocie esta área de color con el código XML de este botón.

**Información sobre herramientas**

Define el texto que se mostrará si el usuario mantiene el mouse sobre el botón. No lo confunda con la imagen emergente que se mostrará. Una información sobre herramientas es un pequeño título de globo que tarda un momento en aparecer. Sin embargo, la imagen de arte del mouse aparecerá al instante en el color y la forma que elija.

**AlHacerClic**

Define el evento que se produce cuando se hace clic con el mouse en el botón. El valor de este atributo de evento se denomina controlador de eventos y será una línea de código de Microsoft JScript o una función de JScript en un archivo de texto externo cargado por el atributo **loadScript** de una **vista**. En este caso, el código JScript llama al método **URL** de Windows Media Player, que carga y comienza a reproducir un archivo llamado "Laure. WMA". Tenga en cuenta que la línea finaliza con un punto y coma dentro de las comillas, que es una buena práctica de codificación de JScript. Tenga en cuenta también el uso de comillas simples dentro de las comillas dobles para establecer el nombre de archivo. Para obtener más información sobre JScript, vea [usar JScript](using-jscript.md) en la sección acerca de las máscaras de este SDK.

Observe que no hay ninguna etiqueta **BUTTONELEMENT** final. Si un elemento no incluye otro elemento, puede cerrarlo con la barra diagonal justo antes del corchete angular de cierre. Esto indica al XML que ha terminado con ese elemento. Por ejemplo,


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



y


```C++
<BUTTONELEMENT/>
```



transmita la misma información en XML.

La eficacia de las máscaras proviene de usar controladores de eventos. Si el usuario realiza alguna acción con un mouse, puede controlar ese evento con JScript. El código puede ser una sola línea que hace que Windows Media Player haga algo sencillo como reproducir, o puede ser una aplicación completa escrita en JScript.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




