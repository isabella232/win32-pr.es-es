---
description: Configuración de la codificación de audio
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Configuración de la codificación de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275140"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a>Configuración de la codificación de audio (Microsoft Media Foundation)

El codificador Windows Media Audio enumera todos los tipos de salida admitidos en su forma completa. Recupere el tipo que desee llamando a **IMediaObject:: GetOutputType** o **IMFTransform:: GetAvailableOutputType** y, a continuación, establezca el tipo recuperado, sin modificar, como el tipo de salida llamando a **IMediaObject:: SetOutputType** o **IMFTransform:: SetOutputType**.

Los tipos de medios de salida que admite el codificador de audio cambian a medida que se configuran las propiedades del codificador. Debe configurar todas las propiedades del codificador que desee usar antes de enumerar el tipo de salida.

Los codificadores de audio admiten los modos de dos pasos y VBR, pero se configuran de forma diferente que para el vídeo. Para obtener más información, consulte [enumeración de tipos de audio para modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md).

Los tipos de entrada admitidos por el codificador de audio no estarán disponibles hasta que se establezca el tipo de salida. Si llama a **IMediaObject:: GetInputType** o **IMFTransform:: GetInputType** antes de establecer un tipo de salida, el método devuelve DMO \_ e \_ no hay \_ más \_ elementos o MFT \_ e \_ no hay \_ más \_ tipos respectivamente. Una vez establecido el tipo de salida, el codificador enumera los tipos de entrada que admite para el tipo de salida seleccionado.

El codificador de Windows Media Audio no realiza ningún muestreo de audio. Esto significa que el tipo de salida del codificador y el tipo de entrada del codificador deben tener el mismo número de canales, bits por muestra y velocidad de muestra. Para obtener más información, vea [Buscar tipos de salida del codificador de audio](findingaudioencoderoutputtypes.md).

> [!Note]  
>    Cada tipo de salida enumerado por el codificador de audio contiene una estructura **WAVEFORMATEX** (señalada por el **tipo de \_ medio am \_ . pbFormat**) con datos extendidos anexados. **WAVEFORMATEX. cbSize** especifica el tamaño de los datos extendidos. Estos datos se deben mantener con el contenido codificado para que se pueda entregar al descodificador. No se puede descomprimir el contenido sin los datos de formato extendido.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



