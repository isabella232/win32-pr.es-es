---
title: Obtener las funcionalidades de un controlador de captura
description: Obtener las funcionalidades de un controlador de captura
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- WM_CAP_DRIVER_GET_CAPS mensaje
- CapDriverGetCaps macro
- CAPDRIVERCAPS (estructura)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d15a3b1e01ccff738494f287126b7e1ab033056
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169626"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a>Obtener las funcionalidades de un controlador de captura

El [**mensaje WM CAP DRIVER GET \_ \_ \_ \_ CAPS**](wm-cap-driver-get-caps.md) devuelve las funciones del controlador de captura y el hardware subyacente en la [**estructura CAPDRIVERCAPS.**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) Cada vez que una aplicación conecta un nuevo controlador de captura a la ventana de captura, debe actualizar la **estructura CAPDRIVERCAPS.** En el ejemplo siguiente se usa [**la macro capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) para obtener las funcionalidades del controlador de captura.


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




