---
title: Obtener el estado de una ventana de captura
description: Obtener el estado de una ventana de captura
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- CapGetStatus (macro)
- Estructura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8effedac3950f0f57aaa6e57ccd5a93fe3044982c3d6ec6d6bb69b56024a1255
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038375"
---
# <a name="obtaining-the-status-of-a-capture-window"></a>Obtener el estado de una ventana de captura

En el ejemplo siguiente se usa la función [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) para establecer el tamaño de la ventana de captura en las dimensiones generales de la secuencia de vídeo entrante en función de la información devuelta por la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) en la [**estructura CAPSTATUS.**](/windows/win32/api/vfw/ns-vfw-capstatus)


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

 

 