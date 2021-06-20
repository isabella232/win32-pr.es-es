---
title: Vista previa de vídeo (Windows Multimedia)
description: En este ejemplo de Windows Multimedia se usa capPreviewRate para establecer la velocidad de visualización de fotogramas para el modo de vista previa y capPreview para poner la ventana de captura en modo de vista previa.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview macro
- capPreviewRate (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc3aaeb9a8ff0f040218fca4822af93ab8bfe29
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405548"
---
# <a name="previewing-video-windows-multimedia"></a><span data-ttu-id="2e711-105">Vista previa de vídeo (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="2e711-105">Previewing Video (Windows Multimedia)</span></span>

<span data-ttu-id="2e711-106">En el ejemplo siguiente se usa la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) para establecer la velocidad de visualización de fotogramas para el modo de vista previa en 66 milisegundos por fotograma y, a continuación, se usa la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) para colocar la ventana de captura en modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="2e711-106">The following example uses the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro to set the frame display rate for preview mode to 66 milliseconds per frame and then uses the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro to place the capture window in preview mode.</span></span>


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a><span data-ttu-id="2e711-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e711-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e711-108">Uso de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="2e711-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




