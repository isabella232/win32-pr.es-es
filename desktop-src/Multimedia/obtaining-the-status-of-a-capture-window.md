---
title: Obtener el estado de una ventana de captura
description: Obtener el estado de una ventana de captura
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- capGetStatus (macro)
- Estructura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f848898247ad8ea2ddbb0dde7a13c08b6a7274
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995166"
---
# <a name="obtaining-the-status-of-a-capture-window"></a><span data-ttu-id="cbc04-105">Obtener el estado de una ventana de captura</span><span class="sxs-lookup"><span data-stu-id="cbc04-105">Obtaining the Status of a Capture Window</span></span>

<span data-ttu-id="cbc04-106">En el ejemplo siguiente se usa la función [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) para establecer el tamaño de la ventana de captura en las dimensiones generales del flujo de vídeo entrante en función de la información devuelta por la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) en la estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) .</span><span class="sxs-lookup"><span data-stu-id="cbc04-106">The following example uses the [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) function to set the size of the capture window to the overall dimensions of the incoming video stream based on information returned by the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro in the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure.</span></span>


```C++
CAPSTATUS CapStatus;

capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS)); 

SetWindowPos(hWndC, NULL, 0, 0, CapStatus.uiImageWidth, 
    CapStatus.uiImageHeight, SWP_NOZORDER | SWP_NOMOVE); 
```



## <a name="related-topics"></a><span data-ttu-id="cbc04-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cbc04-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbc04-108">Uso de la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="cbc04-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 