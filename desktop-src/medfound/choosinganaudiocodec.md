---
description: Elección de un códec de audio
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Elección de un códec de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275146"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a>Elección de un códec de audio (Microsoft Media Foundation)

El [**codificador Windows Media Audio**](windowsmediaaudioencoder.md) proporciona tres categorías de codificación de audio, tal como se muestra en la tabla siguiente.



| Category                         | Propósito                                                    |
|----------------------------------|------------------------------------------------------------|
| Estándar Windows Media Audio     | Compresión de audio de uso general.                      |
| Windows Media Audio Professional | Compresión de audio de varios canales y de alta definición.       |
| Windows Media Audio sin pérdida de     | Comprimir el audio sin perder los datos originales. |



 

La categoría estándar proporciona codificación de audio de uso general adecuada para diversos escenarios de reproducción. Por ejemplo, puede comprimir el audio a una velocidad de bits baja para la transmisión por secuencias a través de una red con ancho de banda limitado o para la representación en dispositivos portátiles. En el otro extremo de la escala, puede generar contenido de audio comprimido para la reproducción de alta calidad. El énfasis de los algoritmos de codificación estándar es la música, pero también es adecuado para otro contenido de audio complejo. La categoría estándar debe ser la predeterminada para el contenido de audio. Las categorías Professional y Lossless deben usarse para satisfacer las necesidades específicas.

Un codificador independiente, el [**codificador de Windows Media Voice**](windowsmediaaudiovoiceencoder.md), proporciona compresión de voz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



