---
title: Cambiar una configuración de captura de vídeo
description: Cambiar una configuración de captura de vídeo
ms.assetid: a5fe7e1e-084d-4102-91d4-ffe5d1d0e5c8
keywords:
- CapCaptureGetSetup macro
- CapCaptureSetSetup macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af4142880fcbd272bc133d7f488afac02928614cfe33be6d209df27ccd1bc76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145118"
---
# <a name="changing-a-video-capture-setting"></a>Cambiar una configuración de captura de vídeo

En el ejemplo siguiente se usan las macros [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) y [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) para cambiar la velocidad de captura del valor predeterminado (15 fotogramas por segundo) a 10 fotogramas por segundo.


```C++
CAPTUREPARMS CaptureParms;
float FramesPerSec = 10.0;

capCaptureGetSetup(hWndC, &CaptureParms, sizeof(CAPTUREPARMS));

CaptureParms.dwRequestMicroSecPerFrame = (DWORD) (1.0e6 / 
    FramesPerSec);
capCaptureSetSetup(hWndC, &CaptureParms, sizeof (CAPTUREPARMS)); 
 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




