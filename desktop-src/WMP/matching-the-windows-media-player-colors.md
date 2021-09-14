---
title: Coincidencia de los colores Reproductor de Windows Media datos
description: Coincidencia de los colores Reproductor de Windows Media datos
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Reproductor de Windows Media en línea, que coinciden Reproductor de Windows Media colores
- tiendas en línea, colores Reproductor de Windows Media coincidencia
- tiendas en línea de tipo 1, que coinciden Reproductor de Windows Media colores
- tiendas en línea de tipo 2, que coinciden Reproductor de Windows Media colores
- Reproductor de Windows Media en línea, Reproductor de Windows Media coincidencia de colores
- tiendas en línea, Reproductor de Windows Media coincidencia de colores
- tiendas en línea de tipo 1, Reproductor de Windows Media coincidencia de colores
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
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967503"
---
# <a name="matching-the-windows-media-player-colors"></a>Coincidencia de los colores Reproductor de Windows Media datos

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



También hay otras propiedades de color disponibles para su uso. Vea External Object for Type 2 Online Stores ( Objeto externo [para almacenes en línea de tipo 2).](external-object-for-type-2-online-stores.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**External.appColorLight**](external-appcolorlight.md)
</dt> <dt>

[**Evento External.OnColorChange**](external-oncolorchange-event.md)
</dt> <dt>

[**Información común a los almacenes en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




