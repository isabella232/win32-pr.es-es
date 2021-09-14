---
title: Descripción (Reproductor de Windows Media SDK)
description: Descripción
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Reproductor de Windows Media Máscaras móviles, sección Descripción
- máscaras, sección Descripción
- referencia de máscaras, sección Descripción
- Sección Descripción en máscaras
- archivos de definición de máscara, sección Descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068478"
---
# <a name="description-windows-media-player-sdk"></a>Descripción (Reproductor de Windows Media SDK)

Al crear una máscara para Reproductor de Windows Media serie 9 para Windows Mobile 2003 o posterior, debe incluir una sección Descripción. La sección Descripción permite especificar el ancho y alto de la pantalla, la resolución de la pantalla y la orientación de la pantalla para la que se diseñó la máscara. La sección Descripción debe aparecer en el archivo de definición de máscara antes que cualquier otra sección y justo después de la declaración de versión inicial.

La sección Descripción del archivo de definición de máscara debe comenzar con la siguiente línea:


```C++
[ Description ]

```



A continuación, debe agregar información sobre las dimensiones de la máscara y la resolución de pantalla. En el ejemplo siguiente se muestra cómo especificar dimensiones:


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



Esto especifica que ha diseñado la máscara para que se muestre a 240 píxeles de ancho, 320 píxeles de alto y con una resolución de pantalla de 96 PPP. Tenga en cuenta que esto implica una orientación en modo vertical.

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

 

Debe tener cuidado de especificar siempre las dimensiones, resolución y orientación correctas para las que se ha escrito la máscara. Por ejemplo, si las dimensiones especificadas por la máscara describen una orientación horizontal, la máscara no estará disponible cuando el dispositivo esté en modo vertical, incluso si especifica Vertical en la línea de orientación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




