---
description: Obtención del código de tiempo del dispositivo
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Obtención del código de tiempo del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787cf328214c1a266b7f129e4e517716b1d04f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061098"
---
# <a name="getting-timecode-from-the-device"></a>Obtención del código de tiempo del dispositivo

Mientras se reproduce una cinta DV o está en modo de pausa de registro, puede recuperar el código de tiempo SMPTE o el número de pista absoluto. Para ello, llame al [**método IAMTimecodeReader::GetTimecode.**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) Este método toma un puntero a una [**estructura TIMECODE \_ SAMPLE,**](/windows/win32/api/strmif/ns-strmif-timecode_sample) que describe el código de tiempo. Antes de llamar al método , inicialice el **miembro dwFlags** de la estructura . Use el valor ED DEVCAP TIMECODE READ para recuperar el código de tiempo o el valor \_ \_ \_ ED \_ DEVCAP \_ ATN READ para recuperar el número \_ de pista absoluto.

El **miembro timecode** de la **estructura TIMECODE \_ SAMPLE** es una estructura TIMECODE. Cuando el método vuelve, el **miembro dwFrames** de la estructura TIMECODE contiene el código de tiempo o el número de seguimiento. Para el código de tiempo, las horas, los minutos, los segundos y los fotogramas se empaquetan en un DWORD como valores decimales codificados binarios (BCD), con el formato *hhmmssff*. Use máscaras de bits para extraer los valores individuales.

En el ejemplo siguiente se recupera el código de tiempo y el número de seguimiento.


```C++
if (MyDevCap.bHasTimecode)
{
    TIMECODE_SAMPLE TimecodeSample;
    TimecodeSample.timecode.dwFrames = 0;
    char szBuf[32];

    TimecodeSample.dwFlags = ED_DEVCAP_TIMECODE_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample),  SUCCEEDED(hr)) 
    {
        DWORD dwTime = TimecodeSample.timecode.dwFrames; // Packed BCD value.
        int hour  = ((dwTime & 0x0F000000) >> 24) + 
                    (10 * ((dwTime & 0xF0000000) >> 28));
        int min   = ((dwTime & 0x0F0000) >> 16) + 
                    (10 * ((dwTime & 0xF00000) >> 20));
        int sec   = ((dwTime & 0x0F00) >> 8) + 
                    (10 * ((dwTime & 0xF000) >> 12));
        int frame = (dwTime & 0x0F) + 
                    (10 * ((dwTime & 0xF0) >> 4));
    }

    TimecodeSample.dwFlags = ED_DEVCAP_ATN_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample), SUCCEEDED(hr)) 
    {
        DWORD dwTrackNumber = TimecodeSample.timecode.dwFrames;
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una cámara dv](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
