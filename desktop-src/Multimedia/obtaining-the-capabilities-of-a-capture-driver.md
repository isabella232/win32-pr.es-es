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
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a><span data-ttu-id="2a018-106">Obtención de las capacidades de un controlador de captura</span><span class="sxs-lookup"><span data-stu-id="2a018-106">Obtaining the Capabilities of a Capture Driver</span></span>

<span data-ttu-id="2a018-107">El [**mensaje \_ Cap \_ Cap \_ driver \_ Get**](wm-cap-driver-get-caps.md) devolverá las capacidades del controlador de captura y el hardware subyacente en la estructura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="2a018-107">The [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span> <span data-ttu-id="2a018-108">Cada vez que una aplicación conecta un nuevo controlador de captura a la ventana de captura, debe actualizar la estructura **CAPDRIVERCAPS** .</span><span class="sxs-lookup"><span data-stu-id="2a018-108">Each time an application connects a new capture driver to the capture window, it should update the **CAPDRIVERCAPS** structure.</span></span> <span data-ttu-id="2a018-109">En el ejemplo siguiente se usa la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) para obtener las capacidades del controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="2a018-109">The following example uses the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro to obtain the capture driver capabilities.</span></span>


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a><span data-ttu-id="2a018-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a018-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a018-111">Uso de la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="2a018-111">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




