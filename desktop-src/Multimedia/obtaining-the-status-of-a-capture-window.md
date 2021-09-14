---
title: Obtener el estado de una ventana de captura
description: Obtener el estado de una ventana de captura
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- CapGetStatus macro
- Capstatus (estructura)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f848898247ad8ea2ddbb0dde7a13c08b6a7274
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169622"
---
# <a name="obtaining-the-status-of-a-capture-window"></a>Obtener el estado de una ventana de captura

En el ejemplo siguiente se usa la función [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) para establecer el tamaño de la ventana de captura en las dimensiones generales de la secuencia de vídeo entrante en función de la información devuelta por la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) en la estructura [**CAPSTATUS.**](/windows/win32/api/vfw/ns-vfw-capstatus)


```C++
CAPSTATUS CapStatus;

capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS)); 

SetWindowPos(hWndC, NULL, 0, 0, CapStatus.uiImageWidth, 
    CapStatus.uiImageHeight, SWP_NOZORDER | SWP_NOMOVE); 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 