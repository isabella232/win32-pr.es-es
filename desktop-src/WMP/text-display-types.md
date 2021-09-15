---
title: Tipos de presentación de texto
description: Tipos de presentación de texto
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Reproductor de Windows Media Máscaras móviles, texto
- texto en máscaras, tipos de visualización
- skins,text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fa8871d889a271bcbc59ce7b3118bc05be2eb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569757"
---
# <a name="text-display-types"></a>Tipos de presentación de texto

No es necesario incluir las pantallas de texto en la máscara, pero hay muchas instancias en las que es posible que quiera. Por ejemplo, es posible que quiera incluir una barra de seguimiento Buscar para permitir al usuario moverse a cualquier posición del elemento multimedia, pero también puede incluir una presentación de texto que muestre el número de segundos transcurridos desde que el elemento multimedia actual empezó a reproducirse.

**Mostrar cuadros**

A continuación se muestran varios atributos que un elemento de texto puede mostrar:

-   Hora
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
-   Status
-   VolPercent

Para obtener más información sobre los tipos de presentación de texto, vea [la sección Texto](text.md) de la referencia de máscara.

**Marco de desplazamiento**

Además de usar los elementos de texto individuales, puede combinar uno o varios atributos en un marco de texto de desplazamiento. Esto resulta útil si desea mostrar una agrupación de información de texto relacionada en un área pequeña. Por ejemplo, podría mostrar información de título, autor y copyright en un marques.

Para obtener más información sobre cómo crear una marquesina de texto, vea la [sección Marquee](marquee.md) de la referencia de máscara.

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
> Cuando se reproduce un elemento multimedia, la pantalla de estado girará a través del subtítulo, el intérprete, el álbum, el género y la velocidad de bits actual.

 

Para obtener información sobre cómo crear una presentación de estado a través del elemento Status, vea la [sección Status](status.md) de la referencia de máscara; Sin embargo, es preferible usar el atributo status en el elemento Text en lugar del elemento Status.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media Funcionalidad móvil**](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 




