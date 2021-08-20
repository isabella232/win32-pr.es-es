---
description: Elección de un códec de audio
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Elegir un códec de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc361f66a069a4c7c0bc895d83d5e705681b7380b2e7ad57efc5501ae89bb16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880721"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a>Elegir un códec de audio (Microsoft Media Foundation)

El [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md) proporciona tres categorías de codificación de audio, como se muestra en la tabla siguiente.



| Category                         | Propósito                                                    |
|----------------------------------|------------------------------------------------------------|
| Windows Media Audio Standard     | Compresión de audio de uso general.                      |
| Windows Audio multimedia Professional | Comprimir audio multicanal y de alta definición.       |
| Windows Audio multimedia sin pérdida de datos     | Comprimir audio sin perder ninguno de los datos originales. |



 

La categoría Estándar proporciona codificación de audio de uso general adecuada para diversos escenarios de reproducción. Por ejemplo, puede comprimir el audio a una velocidad de bits baja para el streaming a través de una red con ancho de banda limitado o para la representación en dispositivos portátiles. En el otro extremo de la escala, puede generar contenido de audio comprimido para una reproducción de alta calidad. El énfasis de los algoritmos de codificación estándar está en la música, pero también son adecuados para otro contenido de audio complejo. La categoría Estándar debe ser la predeterminada para el contenido de audio. Las Professional y sin pérdida de datos deben usarse para satisfacer necesidades específicas.

Un codificador independiente, el Windows [**Media Voice Encoder,**](windowsmediaaudiovoiceencoder.md)proporciona compresión de voz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



