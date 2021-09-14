---
description: Elección de un códec de audio
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Elegir un códec de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269383"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a>Elegir un códec de audio (Microsoft Media Foundation)

El [**Windows Media Audio Encoder proporciona**](windowsmediaaudioencoder.md) tres categorías de codificación de audio, como se muestra en la tabla siguiente.



| Category                         | Propósito                                                    |
|----------------------------------|------------------------------------------------------------|
| Windows Media Audio Standard     | Compresión de audio de uso general.                      |
| Windows Audio multimedia Professional | Comprimir audio multicanal y de alta definición.       |
| Windows Audio multimedia sin pérdida     | Comprimir audio sin perder ninguno de los datos originales. |



 

La categoría Estándar proporciona codificación de audio de uso general adecuada para diversos escenarios de reproducción. Por ejemplo, puede comprimir el audio a una velocidad de bits baja para el streaming a través de una red con ancho de banda limitado o para la representación en dispositivos portátiles. En el otro extremo de la escala, puede generar contenido de audio comprimido para una reproducción de alta calidad. El énfasis de los algoritmos de codificación estándar está en la música, pero también son adecuados para otro contenido de audio complejo. La categoría Estándar debe ser la predeterminada para el contenido de audio. Las Professional y las categorías sin pérdida de datos deben usarse para satisfacer necesidades específicas.

Un codificador independiente, el [**Windows media voice,**](windowsmediaaudiovoiceencoder.md)proporciona compresión de voz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



