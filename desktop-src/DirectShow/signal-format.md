---
description: Formato de señal
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Formato de señal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66add7467f2f497985094c603aaea83b55967f6b2c07eba4cacde080503ef2e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583185"
---
# <a name="signal-format"></a>Formato de señal

El formato de señal de una cámara DV puede ser ÁLISIS o PAL, estándar o de reproducción larga.

**Controlador MSDV**

Para obtener el formato de señal de entrada del controlador MSDV, llame al método [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) y pase la marca \_ ED TRANSBASIC \_ INPUT \_ SIGNAL. El método devuelve una constante definida, que indica el formato.

El código siguiente comprueba el formato de señal y usa este valor para calcular el tiempo medio por fotograma. La variable Mode recibe la constante de formato de señal.


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



Para obtener el formato de señal de salida, llame al mismo método con la marca \_ ED TRANSBASIC \_ OUTPUT \_ SIGNAL.

**Controlador UVC**

Para obtener el formato de señal de entrada o salida del controlador UVC, llame a [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) en el pin y examine el bloque de formato de vídeo. (En el caso de los dispositivos UVC, el código que se muestra en el ejemplo anterior normalmente devuelve ED \_ TRANSBASIC \_ SIGNAL \_ UNKNOWN, por lo que no es confiable).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una cámara dv](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



