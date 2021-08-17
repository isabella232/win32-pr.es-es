---
title: Coincidencia de los Reproductor de Windows Media colores
description: Coincidencia de los Reproductor de Windows Media colores
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Reproductor de Windows Media en línea, que coinciden Reproductor de Windows Media colores
- online stores,matching Reproductor de Windows Media colors
- tiendas en línea de tipo 1, que coinciden Reproductor de Windows Media colores
- tiendas en línea de tipo 2, que coinciden Reproductor de Windows Media colores
- Reproductor de Windows Media en línea, Reproductor de Windows Media coincidencia de colores
- online stores,Reproductor de Windows Media color matching
- tipo 1 tiendas en línea, Reproductor de Windows Media coincidencia de colores
- tipo 2 tiendas en línea, Reproductor de Windows Media coincidencia de colores
- Reproductor de Windows Media en línea, coincidencia de colores para Reproductor de Windows Media
- tiendas en línea, coincidencia de colores para Reproductor de Windows Media
- tiendas en línea de tipo 1, coincidencia de colores para Reproductor de Windows Media
- tiendas en línea de tipo 2, coincidencia de colores para Reproductor de Windows Media
- coincidencia de colores para Reproductor de Windows Media
- colores de Reproductor de Windows Media coincidencia
- Reproductor de Windows Media, colores correspondientes
- Reproductor de Windows Media, coincidencia de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3dbb7ed8b73973d35bc8ad884109c569d1c4738d038cf48f657068c5bde51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135188"
---
# <a name="matching-the-windows-media-player-colors"></a>Coincidencia de los Reproductor de Windows Media colores

Hacer que la página web de la tienda en línea coincida Reproductor de Windows Media combinación de colores es fácil. Simplemente controle **el evento External.OnColorChange.** Para especificar una función para controlar el evento, use código como el siguiente cuando se cargue la página web:


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



Cada vez que el usuario cambia la combinación de colores Reproductor de Windows Media, el reproductor llamará a la función. En el ejemplo siguiente se muestra una función sencilla que establece el fondo de la página web para que coincida con la **propiedad External.appColorLight:**


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



También hay otras propiedades de color disponibles para su uso. Vea [External Object for Type 2 Online Stores (Objeto externo para almacenes en línea de tipo 2).](external-object-for-type-2-online-stores.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**External.appColorLight**](external-appcolorlight.md)
</dt> <dt>

[**Evento External.OnColorChange**](external-oncolorchange-event.md)
</dt> <dt>

[**Información común a las tiendas en línea de tipo 1 y tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




