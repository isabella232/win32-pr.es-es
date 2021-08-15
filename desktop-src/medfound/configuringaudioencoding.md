---
description: Configuración de la codificación de audio
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Configuración de la codificación de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2344808decffd4b50d5926074dbf71d60445580adb4556703367369e1e146d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880370"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a>Configuración de la codificación de audio (Microsoft Media Foundation)

El Windows Media Audio enumera todos sus tipos de salida admitidos en su forma completa. Recupere el tipo que desee llamando a **IMediaObject::GetOutputType** o **ALETransform::GetAvailableOutputType** y, a continuación, establezca el tipo recuperado, sin modificar, como el tipo de salida mediante una llamada a **IMediaObject::SetOutputType** o **ALETransform::SetOutputType**.

Los tipos de medios de salida admitidos por el codificador de audio cambian a medida que se configuran las propiedades del codificador. Debe configurar todas las propiedades del codificador que desea usar antes de enumerar el tipo de salida.

Los codificadores de audio admiten los modos de dos pases y VBR, pero se configuran de forma diferente a para el vídeo. Para obtener más información, vea [Enumerar tipos de audio para modos de codificación específicos.](enumeratingaudiotypesforspecificencodingmodes.md)

Los tipos de entrada admitidos por el codificador de audio no están disponibles hasta que se establece el tipo de salida. Si llama a **IMediaObject::GetInputType** o **ASETRANSFORM::GetInputType** antes de establecer un tipo de salida, el método devuelve DMO E NO MORE ITEMS o \_ \_ \_ \_ MFT \_ E NO MORE TYPES, \_ respectivamente. \_ \_ Una vez establecido el tipo de salida, el codificador enumera los tipos de entrada que admite para el tipo de salida seleccionado.

El codificador Windows Media Audio no realiza ningún Windows de audio multimedia. Esto significa que el tipo de salida del codificador y el tipo de entrada del codificador deben tener el mismo número de canales, bits por muestra y frecuencia de muestreo. Para obtener más información, vea [Búsqueda de tipos de salida del codificador de audio.](findingaudioencoderoutputtypes.md)

> [!Note]  
>    Cada tipo de salida enumerado por el codificador de audio contiene una estructura **DEFORMATEX** (a la que apunta **AM MEDIA \_ \_ TYPE.pbFormat)** con datos extendidos anexados. EL tamaño de los datos extendidos se especifica mediante **EL FORMATOATEX.cbSize**. Estos datos deben mantenerse con el contenido codificado para que se puedan entregar al descodificador. El contenido no se puede descomprimir sin los datos de formato extendido.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



