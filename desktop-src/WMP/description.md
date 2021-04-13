---
title: Descripción (SDK de Windows Media Player)
description: Descripción
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Aspectos de Windows Media Player Mobile, sección Descripción
- aspectos, sección Descripción
- referencia de las máscaras, sección Descripción
- Sección de descripción en máscaras
- archivos de definición de máscara, sección Descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421823"
---
# <a name="description-windows-media-player-sdk"></a>Descripción (SDK de Windows Media Player)

Al crear una máscara para Windows Media Player 9 series para Windows Mobile 2003 o posterior, debe incluir una sección de descripción. La sección Descripción le permite especificar el ancho y el alto de la pantalla, la resolución de pantalla y la orientación de la pantalla para la que se diseñó la máscara. La sección Descripción debe aparecer en el archivo de definición de máscara antes que cualquier otra sección y justo después de la declaración de versión inicial.

La sección de Descripción del archivo de definición de máscara debe comenzar con la línea siguiente:


```C++
[ Description ]

```



A continuación, debe agregar información sobre las dimensiones de la máscara y la resolución de pantalla. En el ejemplo siguiente se muestra cómo especificar dimensiones:


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



Esto especifica que se ha diseñado la máscara para mostrar 240 píxeles de ancho, 320 píxeles de alto y el uso de la resolución de pantalla de PPP de 96. Tenga en cuenta que esto implica una orientación en modo vertical.

Opcionalmente, puede especificar el modo de orientación para el que ha diseñado la máscara en la sección Descripción. En el ejemplo siguiente se muestra cómo especificar la orientación:


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



En la tabla siguiente se muestran los valores que puede usar para la orientación.



| Orientación | Descripción                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| Horizontal   | El ancho de la máscara es mayor que el alto de la máscara. La presentación está orientada horizontalmente.   |
| Vertical    | El alto de la máscara es mayor que el ancho de la máscara. La presentación está orientada verticalmente. |
| Square      | El alto de la máscara es igual al ancho de la máscara. La pantalla no tiene ninguna orientación.                    |



 

> [!Note]  
> Windows Media Player 9 series para Windows Mobile 2003 solo mostrará una máscara determinada cuando la sección de descripción especificada en el archivo de definición de máscara coincida con el estado actual del dispositivo.

 

Debe tener cuidado de especificar siempre las dimensiones, la resolución y la orientación correctas para los que se creó la máscara. Por ejemplo, si las dimensiones especificadas por la máscara describen una orientación horizontal, la máscara no estará disponible cuando el dispositivo esté en modo vertical, aunque especifique vertical en la línea de orientación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




