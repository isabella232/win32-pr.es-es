---
description: Enumeración de tipos de audio para modos de codificación específicos
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Enumerar tipos de audio para modos de codificación específicos (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec311c9ac4d879f8834d50353913e7fad1b6e50a9292a44444bc45376247636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828245"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a>Enumerar tipos de audio para modos de codificación específicos (Microsoft Media Foundation)

Los tipos de medios de entrada y salida aceptados por el codificador de audio están muy estructurados. Debe obtener los tipos de salida admitidos llamando **al método IMediaObject::GetOutputType** o **a IMFTransform::GetOutputType**. Después de obtener un tipo de salida, no debe modificarlo.

Si desea usar un modo de codificación distinto del CBR de un paso, debe establecer el modo y, a continuación, enumerar los tipos de salida para ese modo. el codificador cambia los tipos de salida admitidos en función del modo establecido. Las propiedades que controlan el modo de codificación [**son MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) y [**MFPKEY \_ PASSESUSED.**](mfpkey-passesusedproperty.md) Cuando el modo se establece en el codificador, debe enumerar y seleccionar un tipo de salida, con él sin modificaciones, igual que con CBR.

## <a name="identifying-quality-based-vbr-types"></a>Identificar tipos de VBR basados en calidad

El procedimiento para identificar tipos de VBR basados en la calidad depende de si el codificador actúa como un objeto multimedia DirectX (DMO) o actúa como una transformación de Media Foundation (MFT). Para obtener información sobre cuándo un codificador actúa como un DMO o un MFT, vea las páginas de referencia de códecs individuales en [Objetos de códec](codecobjects.md).

Cuando un codificador de audio actúa como un DMO y configura el codificador para que use VBR de un paso, enumera todos los tipos de salida admitidos. Sin embargo, normalmente querrá seleccionar un tipo DE VBR de un solo paso basado en el parámetro de calidad. El codificador coloca el valor de calidad para los tipos de salida VBR de un paso en el **miembro nAvgBytesPerSec** de la estructura **DESACTEATEX** a la que apunta **DMO MEDIA \_ \_ TYPE.pbFormat**.

Este valor se almacena en el formato siguiente: 0x7FFFFFXX, donde XX es el valor de calidad (de 0 a 100). Por ejemplo, el **valor nAvgBytesPerSec** de 0x7FFFFF62 especifica el nivel de calidad 98 (0x62 = 98).

En el ejemplo siguiente se muestra cómo comprobar el nivel de calidad de un formato cuando el codificador actúa como DMO.


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



Cuando el codificador actúa como MFT y enumera un tipo de salida en una llamada a **GetAvailableOutputType,** puede consultar el MFT para la propiedad **MFPKEY \_ MOST RECENTLY \_ \_ ENUMERATED \_ VBRQUALITY.** El valor devuelto indica la calidad de VBR del tipo de medio de salida devuelto más recientemente. A continuación, puede usar ese valor para establecer la propiedad [**\_ MFPKEY DESIRED \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) del codificador.

## <a name="setting-peak-constraints"></a>Establecer restricciones máximas

Para VBR basado en calidad (un paso) y VBR de dos pases sin restricciones, no se requiere ninguna configuración adicional después de recuperar el tipo de salida. Para usar VBR con restricciones máximas, recupere un tipo de salida con VBR habilitado y dos pases establecidos. Este tipo, sin modificación, describe la configuración de VBR sin restricciones. Para establecer restricciones máximas, establezca las [propiedades \_ MFPKEY RMAX](mfpkey-rmaxproperty.md) y [MFPKEY \_ BMAX.](mfpkey-bmaxproperty.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la codificación de audio](configuringaudioencoding.md)
</dt> <dt>

[Búsqueda de tipos de salida del codificador de audio](findingaudioencoderoutputtypes.md)
</dt> <dt>

[Uso de Two-Pass codificación](usingtwoencodingpasses.md)
</dt> <dt>

[Uso de la codificación VBR](usingvbrencoding.md)
</dt> </dl>

 

 



