---
title: Obtención de las capacidades de un controlador de captura
description: Obtención de las capacidades de un controlador de captura
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- Mensaje WM_CAP_DRIVER_GET_CAPS
- capDriverGetCaps (macro)
- Estructura CAPDRIVERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d15a3b1e01ccff738494f287126b7e1ab033056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676279"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a>Obtención de las capacidades de un controlador de captura

El [**mensaje \_ Cap \_ Cap \_ driver \_ Get**](wm-cap-driver-get-caps.md) devolverá las capacidades del controlador de captura y el hardware subyacente en la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) . Cada vez que una aplicación conecta un nuevo controlador de captura a la ventana de captura, debe actualizar la estructura **CAPDRIVERCAPS** . En el ejemplo siguiente se usa la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) para obtener las capacidades del controlador de captura.


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




