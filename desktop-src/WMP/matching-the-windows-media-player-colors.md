---
title: Coincidencia de los colores de Media Player de Windows
description: Coincidencia de los colores de Media Player de Windows
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player tiendas en línea, que coinciden con los colores de Media Player de Windows
- tiendas en línea, coincidencia de los colores de Media Player de Windows
- tipo 1 almacenes en línea, que coinciden con los colores de Media Player de Windows
- tipo 2 tiendas en línea, coincidencia de Media Player colores de Windows
- Windows Media Player tiendas en línea, coincidencia de color de Windows Media Player
- tiendas en línea, coincidencia de color de Windows Media Player
- tipo 1 almacenes en línea, coincidencia de color de Windows Media Player
- tipo 2 tiendas en línea, coincidencia de color de Windows Media Player
- Windows Media Player tiendas en línea, coincidencia de color para Windows Media Player
- tiendas en línea, coincidencia de color para Windows Media Player
- tipo 1 tiendas en línea, coincidencia de color para Windows Media Player
- tipo 2 tiendas en línea, coincidencia de color para Windows Media Player
- coincidencia de color para Windows Media Player
- coincidencia de los colores de Media Player de Windows
- Media Player de Windows, colores coincidentes
- Media Player de Windows, coincidencia de color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704759"
---
# <a name="matching-the-windows-media-player-colors"></a>Coincidencia de los colores de Media Player de Windows

Hacer que la Página Web de la tienda en línea coincida con la combinación de colores de Windows Media Player es fácil. Simplemente controle el evento **external. OnColorChange** . Para especificar una función que controle el evento, use código similar al siguiente cuando se cargue la página web:


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



Cada vez que el usuario cambia la combinación de colores de Windows Media Player, el reproductor llamará a la función. En el ejemplo siguiente se muestra una función simple que establece el fondo de la página web para que coincida con la propiedad **external. appColorLight** :


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



También hay otras propiedades de color disponibles para su uso. Vea el [objeto externo para las tiendas en línea de tipo 2](external-object-for-type-2-online-stores.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**External. appColorLight**](external-appcolorlight.md)
</dt> <dt>

[**Evento external. OnColorChange**](external-oncolorchange-event.md)
</dt> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




