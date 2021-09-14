---
title: Adición de Play BUTTONELEMENT
description: Adición de Play BUTTONELEMENT
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- crear máscaras,elemento BUTTONELEMENT
- Reproductor de Windows Media máscaras, elemento BUTTONELEMENT
- skins,BUTTONELEMENT, elemento
- archivos de definición de máscara, elemento BUTTONELEMENT
- Elemento BUTTONELEMENT
- elements,BUTTONELEMENT
- crear máscaras, botones de reproducción
- Reproductor de Windows Media máscaras, botones reproducir
- máscaras, botones de reproducción
- archivos de definición de máscara, botones reproducir
- Botones de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374315"
---
# <a name="adding-the-play-buttonelement"></a>Adición de Play BUTTONELEMENT

Por último, puede agregar los elementos **BUTTONELEMENT** que conectan los botones visuales de la pantalla a Reproductor de Windows Media acciones. Este es el núcleo de la máscara y se puede pensar que se trata de conectar la superficie de la máscara a la maquinaria interna de Reproductor de Windows Media.

**Los elementos BUTTONELEMENT** están incluidos dentro de **buttongroup.** Siempre debe tener al menos un **BUTTONELEMENT** dentro de **cada BUTTONGROUP.**

Coloque el código **PLAY BUTTONELEMENT** después del corchete angular de cierre **de BUTTONGROUP.**


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



Los atributos siguientes se usan para definir **BUTTONELEMENT** para el botón Reproducir:

**mappingColor**

Este es el valor de color de una región en el archivo de creación de mapas que creó antes. En este caso, es el color verde sólido. Este atributo es necesario para cualquier **BUTTONELEMENT.** Al definir este color, se le Reproductor de Windows Media que asocie esta área de color con el código XML de este botón.

**upToolTip**

Esto define el texto que se mostrará si el usuario mantiene el mouse sobre el botón. No confunda esto con la imagen de mantener el puntero que se mostrará. Una información sobre herramientas es un título de globo pequeño que tarda un momento en aparecer. Sin embargo, la imagen de mantener el puntero sobre el puntero aparecerá al instante en el color y la forma que elija.

**Onclick**

Esto define el evento que tiene lugar cuando el mouse hace clic en el botón. El valor de este atributo de evento se denomina controlador de eventos y será una línea de código de Microsoft JScript o una función JScript en un archivo de texto externo cargado por el atributo **loadScript** de una **vista**. En este caso, el JScript llama al método **url** de Reproductor de Windows Media, que carga y comienza a reproducir un archivo denominado "laure.wma". Tenga en cuenta que la línea termina con un punto y coma dentro de las comillas, lo que es JScript práctica de codificación. Tenga en cuenta también el uso de comillas simples dentro de las comillas dobles para establecer el nombre de archivo. Para obtener más información JScript, consulte [Uso de JScript](using-jscript.md) en la sección Acerca de las máscaras de este SDK.

Observe que no hay ninguna etiqueta **BUTTONELEMENT final.** Si un elemento no incluye otro elemento, puede cerrarlo con la barra diagonal justo antes del corchete angular de cierre. Esto indica a XML que ha terminado con ese elemento. Por ejemplo,


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



y


```C++
<BUTTONELEMENT/>
```



transmitir la misma información en XML.

La potencia de las máscaras proviene del uso de controladores de eventos. Si el usuario hace algo con un mouse, puede controlar ese evento con JScript. El código puede ser una sola línea que Reproductor de Windows Media hacer algo sencillo como reproducir, o bien puede ser una aplicación completa escrita en JScript.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación del archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




