---
title: Vista previa de vídeo (Windows Multimedia)
description: En este ejemplo de Windows Multimedia usa capPreviewRate para establecer la velocidad de visualización de fotogramas para el modo de vista previa y capPreview para poner la ventana de captura en modo de vista previa.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview macro
- capPreviewRate (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc3aaeb9a8ff0f040218fca4822af93ab8bfe29
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371551"
---
# <a name="previewing-video-windows-multimedia"></a>Vista previa de vídeo (Windows Multimedia)

En el ejemplo siguiente se usa la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) para establecer la velocidad de visualización de fotogramas para el modo de vista previa en 66 milisegundos por fotograma y, a continuación, se usa la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) para colocar la ventana de captura en modo de vista previa.


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

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




