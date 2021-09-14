---
title: Crear una ventana de captura
description: Crear una ventana de captura
ms.assetid: a727ce14-9b12-4f21-bab4-fa2eb245dce7
keywords:
- Función capCreateCaptureWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28375da063839d3120ca60bdabd5ca997fa31b02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071801"
---
# <a name="creating-a-capture-window"></a>Crear una ventana de captura

En el ejemplo siguiente se crea una ventana de captura mediante la [**función capCreateCaptureWindow.**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)


```C++
hWndC = capCreateCaptureWindow (
    TEXT("My Capture Window"),   // window name if pop-up 
    WS_CHILD | WS_VISIBLE,       // window style 
    0, 0, 160, 120,              // window position and dimensions
    (HWND) hwndParent, 
    (int) nID /* child ID */); 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




