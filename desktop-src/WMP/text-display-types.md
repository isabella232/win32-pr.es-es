---
title: Tipos de presentación de texto
description: Tipos de presentación de texto
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Aspectos de Windows Media Player Mobile, texto
- texto en máscaras, tipos de presentación
- máscaras, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fa8871d889a271bcbc59ce7b3118bc05be2eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775102"
---
# <a name="text-display-types"></a>Tipos de presentación de texto

No es necesario incluir presentaciones de texto en la máscara, pero hay muchos casos en los que es posible que desee. Por ejemplo, puede que desee incluir una barra de Inicio Buscar para permitir que el usuario se mueva a cualquier posición del elemento multimedia, pero también puede incluir una presentación de texto que muestre el número de segundos transcurridos desde que el elemento multimedia actual comenzó a reproducirse.

**Cuadros de presentación**

A continuación se muestran varios atributos que un elemento de texto puede mostrar:

-   Hora
-   Lista de reproducción
-   Dar\#
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

Para obtener más información sobre los tipos de presentación de texto, vea la sección de [texto](text.md) de la referencia de máscara.

**Marquesina de desplazamiento**

Además de usar los elementos de texto individuales, puede combinar uno o varios atributos en una marquesina de texto de desplazamiento. Esto resulta útil si desea mostrar una agrupación de información de texto relacionada en un área pequeña. Por ejemplo, puede mostrar información sobre el título, el autor y el copyright en una marquesina.

Para obtener más información sobre cómo crear una marquesina de texto, vea la sección [marquesina](marquee.md) de la referencia de máscara.

**Pantalla de estado**

Otro tipo de visualización de texto es la presentación del estado. Esto le permite mostrar automáticamente información sobre el estado actual de Windows Media Player Mobile. Por ejemplo, la pantalla de Estado informará al usuario cuando un elemento multimedia está almacenando en búfer para que sea evidente que el reproductor está funcionando.

Los mensajes siguientes aparecen en la pantalla de estado:

-   de respuesta
-   Connecting
-   En pausa
-   Reproduciendo
-   Ready
-   Detenido

> [!Note]  
> Cuando se reproduce un elemento multimedia, la pantalla de estado girará a través del subtítulo, el intérprete, el álbum, el género y la velocidad de bits actual.

 

Para obtener información sobre cómo crear una visualización de estado a través del elemento status, vea la sección [status](status.md) de la referencia de la máscara. sin embargo, es preferible usar el atributo status en el elemento Text en lugar del elemento status.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Funcionalidad de Windows Media Player Mobile**](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 




