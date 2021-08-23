---
description: Uso del códec de Windows media audio
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Uso del códec de Windows media audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e53c84a6915b8bc118015f1524e5126085e7ac199cc4726c88739b0a82738d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972674"
---
# <a name="using-the-windows-media-audio-voice-codec"></a>Uso del códec de Windows media audio

El códec Windows Media Audio Voice proporciona compresión de baja velocidad de bits optimizada para el audio que contiene voz. La capacidad del códec para producir muestras tan pequeñas se debe al intervalo de frecuencia limitado de los sonidos de la voz humana. Esta optimización significa que un codificador de voz dedicado crea una salida de baja calidad para el contenido que contiene sonidos más complicados, como la música. Sin embargo, el códec Windows Media Audio Voice compensa este posible problema de calidad al proporcionar modos independientes para la voz, la música y el contenido mixto. El códec analiza el contenido mixto para determinar qué modo usar para cada parte del archivo.

El códec Windows Media Audio Voice se implementa en el objeto de codificador identificado por el identificador de clase CLSID CWMSPEncMediaObject2 y en el objeto descodificador identificado por el identificador de clase \_ CLSID \_ CWMSPDecMediaObject. La etiqueta de formato de los tipos de medios que usan este códec es 0x00A.

## <a name="configuring-the-encoder"></a>Configuración del codificador

El codificador de voz admite tres modos: voz, música y mezcla. Cada modo está optimizado para obtener los mejores resultados para ese tipo de contenido. Puede configurar el modo del codificador de voz mediante los métodos de **IPropertyStore** para establecer la propiedad [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode.](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md)

Cuando se configura para contenido mixto, el códec Windows Media Audio Voice detectará automáticamente fragmentos de música en el contenido. Si no está satisfecho con los resultados, puede especificar la ubicación de la música en el contenido mediante una lista de decisión de edición (EDL). Para obtener más información, vea [Usar una lista de decisión de edición para codificar voz.](usingavoiceeditingdecisionlist.md)

A diferencia de los demás codificadores de audio, puede establecer el valor de la ventana de búfer para el contenido de voz mediante la propiedad [ \_ MFPKEY WMAVOICE \_ ENC \_ BufferWindow.](mfpkey-wmavoice-enc-bufferwindowproperty.md) Sin embargo, los valores predeterminados deberían funcionar bien en la mayoría de los casos.

> [!Note]  
>    Al configurar el codificador de voz, es muy importante que establezca el tipo de salida antes de establecer el tipo de entrada. Este es el orden recomendado de las operaciones para todos los códecs de audio, pero el codificador de voz puede notificar tipos de salida erróneos si se establece una entrada al llamar a **IMediaObject::GetOutputType** o **a IMFTransform::GetOutputType**.

 

## <a name="decoding"></a>Descodificación

No hay ningún requisito especial para la decodificación de audio de voz. Para obtener más información, vea [Configuring Audio Decoding](configuringaudiodecoding.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



