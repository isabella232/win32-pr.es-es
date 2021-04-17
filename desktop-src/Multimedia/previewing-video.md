---
title: Obtener una vista previa del vídeo (Windows multimedia)
description: Obtener una vista previa del vídeo
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview (macro)
- capPreviewRate (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79c8e24d30fd5141b5b1ac14de99d83e0b2bc620
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676537"
---
# <a name="previewing-video-windows-multimedia"></a>Obtener una vista previa del vídeo (Windows multimedia)

En el ejemplo siguiente se usa la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) para establecer la velocidad de presentación del fotograma para el modo de vista previa en 66 milisegundos por fotograma y, a continuación, se usa la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) para colocar la ventana de captura en modo de vista previa.


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




