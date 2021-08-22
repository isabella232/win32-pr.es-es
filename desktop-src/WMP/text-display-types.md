---
title: Tipos de presentación de texto
description: Tipos de presentación de texto
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Reproductor de Windows Media Máscaras móviles, texto
- texto en máscaras, tipos de visualización
- máscaras, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01826f35db0d3877a3ecd34c351315872760b1b9b0713a36955bb3161ed6ba8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134608"
---
# <a name="text-display-types"></a>Tipos de presentación de texto

No es necesario incluir pantallas de texto en la máscara, pero hay muchas instancias en las que es posible que quiera. Por ejemplo, es posible que quiera incluir una barra de seguimiento Buscar para permitir que el usuario se mueva a cualquier posición del elemento multimedia, pero también puede incluir una presentación de texto que muestre el número de segundos transcurridos desde que el elemento multimedia actual empezó a reproducirse.

**Cuadros para mostrar**

A continuación se muestran varios atributos que puede mostrar un elemento de texto:

-   Time
-   Lista de reproducción
-   Pista\#
-   \#Pistas
-   Título
-   Autor
-   Copyright
-   Nombre de archivo
-   FilenameExt
-   Bitrate
-   Frecuencia
-   Estado
-   VolPercent

Para obtener más información sobre los tipos de presentación de texto, vea [la sección Texto](text.md) de la referencia de máscara.

**Desplazamiento de marquesina**

Además de usar los elementos de texto individuales, puede combinar uno o varios atributos en un marco de texto de desplazamiento. Esto resulta útil si desea mostrar una agrupación de información de texto relacionada en un área pequeña. Por ejemplo, puede mostrar información de título, autor y copyright en un marques.

Para obtener más información sobre cómo crear un marco de texto, consulte la [sección Marquee](marquee.md) de la Referencia de máscara.

**Presentación de estado**

Otro tipo de presentación de texto es la presentación de estado. Esto le permite mostrar automáticamente información sobre el estado actual de Reproductor de Windows Media Mobile. Por ejemplo, la presentación de estado informará al usuario cuando un elemento multimedia se almacena en búfer para que sea evidente que el reproductor está funcionando.

Los mensajes siguientes aparecen en la pantalla de estado:

-   de respuesta
-   Connecting
-   En pausa
-   Reproduciendo
-   Ready
-   Detenido

> [!Note]  
> Cuando se reproduce un elemento multimedia, la presentación de estado gira a través del subtítulo, el intérprete, el álbum, el género y la velocidad de bits actual.

 

Para obtener información sobre cómo crear una presentación de estado a través del elemento Status, vea la [sección Estado](status.md) de la Referencia de máscara; sin embargo, es preferible usar el atributo status en el elemento Text en lugar del elemento Status.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media Funcionalidad móvil**](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 




