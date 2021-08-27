---
title: Vista previa de vídeo (Windows Multimedia)
description: En este ejemplo de Windows Multimedia se usa capPreviewRate para establecer la velocidad de visualización de fotogramas para el modo de vista previa y capPreview para poner la ventana de captura en modo de vista previa.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview macro
- capPreviewRate (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e70d0520af3bb71906c6b0ea4d1c0a61464559eedfd2385753b228841fa6af4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037915"
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

 

 




