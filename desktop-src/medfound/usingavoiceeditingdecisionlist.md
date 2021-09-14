---
description: Usar una lista de decisión de edición para codificar voz
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Usar una lista de decisión de edición para codificar voz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363678"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a>Usar una lista de decisión de edición para codificar voz

Una lista de decisión de edición (EDL) son datos que se proporcionan a un códec que proporciona información sobre cómo se deben codificar partes específicas del contenido. El códec Windows Media Audio 9 Voice admite un EDL simple en el que puede especificar las partes del contenido que contienen música. De forma predeterminada, el códec detecta fragmentos de música cuando se configura para codificar contenido mixto. Solo debe usar una EDL si el códec no detecta correctamente los tipos de contenido.

Para usar un EDL, el codificador de voz debe establecerse para codificar contenido mixto. Configure el modo del códec de voz en "mixto" estableciendo la propiedad [ \_ MFPKEY WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) en 2. Establezca el EDL mediante la [propiedad \_ MFPKEY WMAVOICE \_ ENC \_ EDL.](mfpkey-wmavoice-enc-edlproperty.md) El valor de esta propiedad es una cadena que contiene una lista delimitada por comas de los intervalos de tiempo del contenido que se deben codificar como música. El primer elemento de la lista es la versión de EDL, que siempre es 1. El segundo elemento es el número de secciones de música descritas en la lista. Después del segundo elemento hay varios pares de valores iguales al segundo elemento; Cada par de valores describe el punto inicial y final de un fragmento de música en el contenido, en milisegundos.

Por ejemplo, la cadena EDL "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" especifica cuatro fragmentos de música, cada uno de los cuales tiene una longitud de un segundo. Si la información de la cadena EDL no es válida, se omite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del códec de Windows Media Audio 9](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



