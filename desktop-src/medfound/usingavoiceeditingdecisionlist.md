---
description: Usar una lista de decisiones de edición para la codificación de voz
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Usar una lista de decisiones de edición para la codificación de voz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666869"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a>Usar una lista de decisiones de edición para la codificación de voz

Una lista de decisiones de edición (EDL) es un dato dado a un códec que proporciona información sobre cómo se deben codificar determinadas partes del contenido. El códec de voz de Windows Media Audio 9 admite una EDL simple en la que puede especificar las partes de contenido que contienen música. De forma predeterminada, el códec detecta los pasajes de música en sí cuando se configura para codificar contenido mixto. Solo debe usar una EDL si el códec no detecta los tipos de contenido correctamente.

Para usar una EDL, el codificador de voz debe estar establecido para codificar contenido mixto. Configure el modo del códec de voz en "Mixed" estableciendo la propiedad [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) en 2. Establezca la EDL mediante la propiedad [MFPKEY \_ WMAVOICE \_ enc \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) . El valor de esta propiedad es una cadena que contiene una lista delimitada por comas de los intervalos de tiempo en el contenido que se debe codificar como música. El primer elemento de la lista es la versión de la EDL, que es siempre 1. El segundo elemento es el número de secciones de música descritas en la lista. Después del segundo elemento hay un número de pares de valores igual al segundo elemento; cada par de valores describe el punto inicial y final de un pasaje de música en el contenido, en milisegundos.

Por ejemplo, la cadena de EDL "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" especifica cuatro pasajes musicales, cada uno de los cuales tiene una segunda duración. Si la información de la cadena de EDL no es válida, se omite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el códec de voz de Windows Media Audio 9](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



