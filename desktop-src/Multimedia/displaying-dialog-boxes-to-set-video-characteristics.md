---
title: Mostrar cuadros de diálogo para establecer características de vídeo
description: Mostrar cuadros de diálogo para establecer características de vídeo
ms.assetid: 8074f7d1-e8ab-46c3-acc2-a18be0eb4cc7
keywords:
- CAPDRIVERCAPS (estructura)
- CapDriverGetCaps macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e6ebfa0f75f4bcec63a693636085f16c342e53761b2cb1e67a0e2536fa5cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144478"
---
# <a name="displaying-dialog-boxes-to-set-video-characteristics"></a>Mostrar cuadros de diálogo para establecer características de vídeo

Cada controlador de captura puede proporcionar hasta tres cuadros de diálogo diferentes que se usan para controlar aspectos del proceso de digitalización y captura de vídeo. En el ejemplo siguiente se muestra cómo mostrar estos cuadros de diálogo. Antes de mostrar cada cuadro de diálogo, el ejemplo llama a la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) y comprueba la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) devuelta para ver si el controlador de captura puede mostrarla.


```C++
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

CAPDRIVERCAPS CapDriverCaps = { }; 
CAPSTATUS     CapStatus = { };

capDriverGetCaps(hWndC, &CapDriverCaps, sizeof(CAPDRIVERCAPS)); 
 
// Video source dialog box. 
if (CapDriverCaps.fHasDlgVideoSource)
{
    capDlgVideoSource(hWndC); 
}
 
// Video format dialog box. 
if (CapDriverCaps.fHasDlgVideoFormat) 
{
    capDlgVideoFormat(hWndC); 

    // Are there new image dimensions?
    capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS));

    // If so, notify the parent of a size change.
} 
 
// Video display dialog box. 
if (CapDriverCaps.fHasDlgVideoDisplay)
{
    capDlgVideoDisplay(hWndC); 
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> <dt>

[**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)
</dt> </dl>

 

 




