---
title: Habilitación de la superposición de vídeo
description: Habilitación de la superposición de vídeo
ms.assetid: f0b4f24c-3e35-4a18-ac77-8cae7083b0fe
keywords:
- CapDriverGetCaps macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 961a26a3a78d9153dd024b271179d6971bca6f610ee0fde070e13454e02f8528
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988779"
---
# <a name="enabling-video-overlay"></a>Habilitación de la superposición de vídeo

En el ejemplo siguiente se usa la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) para determinar si un controlador de captura tiene funcionalidades de superposición; Si es así, la macro habilita la superposición.


```C++
CAPDRIVERCAPS CapDrvCaps; 

capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 

if (CapDrvCaps.fHasOverlay) 
    capOverlay(hWndC, TRUE);
 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




