---
description: Formato de señal
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Formato de señal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906664"
---
# <a name="signal-format"></a>Formato de señal

El formato de señal de una videocámara DV puede ser NTSC o PAL, estándar o de larga ejecución.

**Controlador MSDV**

Para obtener el formato de la señal de entrada desde el controlador MSDV, llame al método [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) y pase la \_ marca Ed transbasic \_ Input \_ Signal. El método devuelve una constante definida, que indica el formato.

En el código siguiente se comprueba el formato de la señal y se usa este valor para calcular el tiempo medio por fotograma. El modo variable recibe la constante de formato de señal.


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



Para obtener el formato de la señal de salida, llame al mismo método con la \_ marca Ed transbasic \_ Output \_ Signal.

**Controlador UVC**

Para obtener el formato de señal de entrada o salida del controlador UVC, llame a [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) en el PIN y examine el bloque de formato de vídeo. (En el caso de los dispositivos UVC, el código que se muestra en el ejemplo anterior suele devolver ED \_ \_Señal de transbasic \_ desconocida, por lo que no es confiable).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una videocámara DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



