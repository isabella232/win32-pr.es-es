---
title: Descripción (Reproductor de Windows Media SDK)
description: Descripción
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Reproductor de Windows Media Máscaras móviles, sección Descripción
- máscaras, sección Descripción
- referencia de máscaras, sección Descripción
- Sección descripción en máscaras
- archivos de definición de máscara, sección Descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ca5235939352ffabb924aaf38a706b436d4c1358a92b9aef4996614c53623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749962"
---
# <a name="description-windows-media-player-sdk"></a>Descripción (Reproductor de Windows Media SDK)

Al crear una máscara para Reproductor de Windows Media serie 9 para Windows Mobile 2003 o posterior, debe incluir una sección Descripción. La sección Descripción permite especificar el ancho y alto de la pantalla, la resolución de la pantalla y la orientación de la pantalla para la que se diseñó la máscara. La sección Descripción debe aparecer en el archivo de definición de máscara antes de cualquier otra sección y justo después de la declaración de versión inicial.

La sección Descripción del archivo de definición de máscara debe comenzar con la línea siguiente:


```C++
[ Description ]

```



A continuación, debe agregar información sobre las dimensiones de la máscara y la resolución de pantalla. En el ejemplo siguiente se muestra cómo especificar dimensiones:


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



Esto especifica que ha diseñado la máscara para que se muestre con 240 píxeles de ancho, 320 píxeles de alto y con una resolución de pantalla de 96 PPP. Tenga en cuenta que esto implica una orientación en modo vertical.

Opcionalmente, puede especificar el modo de orientación para el que diseñó la máscara en la sección de descripción. En el ejemplo siguiente se muestra cómo especificar la orientación:


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



En la tabla siguiente se enumeran los valores que puede usar para Orientation.



| Orientación | Descripción                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| Horizontal   | El ancho de la máscara es mayor que el alto de la máscara. La pantalla está orientada de forma horizontal.   |
| Vertical    | El alto de la máscara es mayor que el ancho de la máscara. La pantalla está orientada de forma vertical. |
| Square      | El alto de la máscara es igual al ancho de la máscara. La pantalla no tiene orientación.                    |



 

> [!Note]  
> Reproductor de Windows Media serie 9 para Windows Mobile 2003 solo mostrará una máscara determinada cuando la sección de descripción especificada en el archivo de definición de máscara coincida con el estado actual del dispositivo.

 

Debe tener cuidado de especificar siempre las dimensiones, la resolución y la orientación correctas para las que se autorizó la máscara. Por ejemplo, si las dimensiones especificadas por la máscara describen una orientación horizontal, la máscara no estará disponible cuando el dispositivo esté en modo vertical, incluso si especifica Vertical en la línea de orientación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




