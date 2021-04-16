---
description: Usar el códec Windows Media Audio Voice
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Usar el códec Windows Media Audio Voice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547315"
---
# <a name="using-the-windows-media-audio-voice-codec"></a>Usar el códec Windows Media Audio Voice

El códec Windows Media Audio Voice proporciona compresión de baja velocidad de bits optimizada para audio que contiene voz. La capacidad del códec para generar ejemplos pequeños se debe al intervalo de frecuencias limitado de los sonidos de la voz humana. Esta optimización significa que un codificador de voz dedicado crea una salida de mala calidad para el contenido que contiene sonidos más complicados, como música. Sin embargo, el códec de voz de Windows Media Audio compensa este posible problema de calidad al proporcionar modos independientes de voz, música y contenido mixto. El códec analiza el contenido mixto para determinar el modo que se va a utilizar para cada parte del archivo.

El códec de Windows Media Audio Voice se implementa en el objeto Encoder identificado por el identificador de clase CLSID \_ CWMSPEncMediaObject2 y en el objeto descodificador identificado por el identificador de clase CLSID \_ CWMSPDecMediaObject. La etiqueta de formato de los tipos de medios que usan este códec es 0x00A.

## <a name="configuring-the-encoder"></a>Configurar el codificador

El codificador de voz admite tres modos: voz, música y mixto. Cada modo está optimizado para obtener los mejores resultados para ese tipo de contenido. Puede configurar el modo del codificador de voz mediante los métodos de **IPropertyStore** para establecer la propiedad MFPKEY de [ \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) .

Cuando se configura para contenido mixto, el códec de Windows Media Audio Voice detectará automáticamente el paso de música en el contenido. Si no está satisfecho con los resultados, puede especificar la ubicación de la música en el contenido mediante una lista de decisiones de edición (EDL). Para obtener más información, consulte [uso de una lista de decisiones de edición para la codificación de voz](usingavoiceeditingdecisionlist.md).

A diferencia de los otros codificadores de audio, puede establecer el valor de la ventana de búfer para el contenido de voz mediante la propiedad [MFPKEY \_ WMAVOICE \_ enc \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) . Sin embargo, los valores predeterminados deben funcionar correctamente en la mayoría de los casos.

> [!Note]  
>    Al configurar el codificador de voz, es muy importante que establezca el tipo de salida antes de establecer el tipo de entrada. Este es el orden recomendado de las operaciones para todos los códecs de audio, pero el codificador de voz puede informar de los tipos de salida erróneos si se establece una entrada cuando se llama a **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**.

 

## <a name="decoding"></a>Descodificación

No hay ningún requisito especial para descodificar el audio de voz. Obtener más información, consulte [configuración de la descodificación de audio](configuringaudiodecoding.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



