---
description: Formato de señal
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Formato de señal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375207"
---
# <a name="signal-format"></a>Formato de señal

El formato de señal de una cámara DV puede ser JPEG o PAL, estándar o de reproducción larga.

**Controlador MSDV**

Para obtener el formato de señal de entrada del controlador MSDV, llame al método [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) y pase la marca ED \_ TRANSBASIC \_ INPUT \_ SIGNAL. El método devuelve una constante definida, que indica el formato.

El código siguiente comprueba el formato de señal y usa este valor para calcular el tiempo medio por fotograma. La variable Mode recibe la constante signal-format.


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



Para obtener el formato de señal de salida, llame al mismo método con la marca ED \_ TRANSBASIC \_ OUTPUT \_ SIGNAL.

**Controlador UVC**

Para obtener el formato de señal de entrada o salida del controlador UVC, llame a [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) en el pin y examine el bloque de formato de vídeo. (En el caso de los dispositivos UVC, el código que se muestra en el ejemplo anterior normalmente devuelve ED \_ TRANSBASIC \_ SIGNAL \_ UNKNOWN, por lo que no es confiable).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una videocamba de DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



