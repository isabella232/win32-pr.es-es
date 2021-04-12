---
description: Enumeración de los tipos de audio para los modos de codificación específicos
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Enumeración de los tipos de audio para los modos de codificación específicos (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423536"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a>Enumeración de los tipos de audio para los modos de codificación específicos (Microsoft Media Foundation)

Los tipos de medios de entrada y salida aceptados por el codificador de audio están muy estructurados. Debe obtener los tipos de salida admitidos mediante una llamada al método **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**. Después de obtener un tipo de salida, no debe modificarlo.

Si desea utilizar un modo de codificación que no sea un CBR de un paso, debe establecer el modo y, a continuación, enumerar los tipos de salida para ese modo. el codificador cambia los tipos de salida admitidos en función del conjunto de modos. Las propiedades que controlan el modo de codificación son [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) y [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md). Cuando el modo se establece en el codificador, debe enumerar y seleccionar un tipo de salida, y usarlo sin alteración, al igual que con CBR.

## <a name="identifying-quality-based-vbr-types"></a>Identificar tipos VBR basados en calidad

El procedimiento para identificar tipos VBR basados en la calidad depende de si el codificador actúa como un objeto multimedia de DirectX (DMO) o actúa como una transformación de Media Foundation (MFT). Para obtener información sobre cuándo un codificador actúa como DMO o MFT, consulte las páginas de referencia de códecs individuales en [objetos de códec](codecobjects.md).

Cuando un codificador de audio actúa como DMO y configura el codificador para usar VBR de un paso, enumera todos los tipos de salida admitidos. Sin embargo, normalmente querrá seleccionar un tipo VBR de una sola fase basándose en el parámetro Quality. El codificador coloca el valor de calidad de los tipos de salida VBR de una sola fase en el miembro **nAvgBytesPerSec** de la estructura **WAVEFORMATEX** señalada por el **tipo de \_ medio DMO \_ . pbFormat**.

Este valor se almacena en el siguiente formato: 0x7FFFFFXX, donde XX es el valor de calidad (de 0 a 100). Por ejemplo, el valor **nAvgBytesPerSec** de 0x7FFFFF62 especifica el nivel de calidad 98 (0x62 = 98).

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



Cuando el codificador actúa como MFT y enumera un tipo de salida en una llamada a **GetAvailableOutputType**, puede consultar la MFT para la propiedad **\_ \_ \_ \_ VBRQUALITY enumerada más recientemente MFPKEY** . El valor devuelto indica la calidad VBR del tipo de medio de salida devuelto más recientemente. Después, puede usar ese valor para establecer la [**propiedad \_ \_ VBRQUALITY deseada de MFPKEY**](mfpkey-desired-vbrqualityproperty.md) del codificador.

## <a name="setting-peak-constraints"></a>Establecer restricciones de pico

En el caso de VBR basada en la calidad (un paso) y una VBR de dos pasos sin restricciones, no se requiere ninguna configuración adicional después de recuperar el tipo de salida. Para usar VBR máxima restringida, recupere un tipo de salida con VBR habilitada y dos pasos establecidos. Este tipo, sin modificación, describe la configuración de VBR no restringida. Para establecer las restricciones de pico, establezca las propiedades [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) y [MFPKEY \_ Bmax](mfpkey-bmaxproperty.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la codificación de audio](configuringaudioencoding.md)
</dt> <dt>

[Búsqueda de tipos de salida del codificador de audio](findingaudioencoderoutputtypes.md)
</dt> <dt>

[Uso de la codificación de Two-Pass](usingtwoencodingpasses.md)
</dt> <dt>

[Usar la codificación VBR](usingvbrencoding.md)
</dt> </dl>

 

 



