---
description: Usar una lista de decisión de edición para codificar voz
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Usar una lista de decisión de edición para codificar voz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a2809c30a985ce1c5e81667d2908175100f2690e8453f6166d1717318ec03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688719"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a>Usar una lista de decisión de edición para codificar voz

Una lista de decisión de edición (EDL) son datos que se proporcionan a un códec que proporciona información sobre cómo se deben codificar partes específicas del contenido. El Windows Media Audio 9 Voice admite un sencillo EDL en el que puede especificar las partes del contenido que contienen música. De forma predeterminada, el códec detecta fragmentos de música cuando se configura para codificar contenido mixto. Solo debe usar una EDL si el códec no detecta correctamente los tipos de contenido.

Para usar una EDL, el codificador de voz debe establecerse para codificar contenido mixto. Configure el modo del códec de voz en "mixto" estableciendo la propiedad [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) en 2. Establezca la EDL mediante la [propiedad \_ \_ \_ EDL MFPKEY WMAVOICE ENC.](mfpkey-wmavoice-enc-edlproperty.md) El valor de esta propiedad es una cadena que contiene una lista delimitada por comas de los intervalos de tiempo del contenido que se debe codificar como música. El primer elemento de la lista es la versión de EDL, que siempre es 1. El segundo elemento es el número de secciones de música descritas en la lista. Después del segundo elemento hay varios pares de valores iguales al segundo elemento; cada par de valores describe el punto inicial y final de un fragmento de música en el contenido, en milisegundos.

Por ejemplo, la cadena EDL "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" especifica cuatro fragmentos de música, cada uno de los cuales tiene una longitud de un segundo. Si la información de la cadena EDL no es válida, se omite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del códec de Windows Media Audio 9](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



