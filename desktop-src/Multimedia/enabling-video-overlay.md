---
title: Habilitación de la superposición de vídeo
description: Habilitación de la superposición de vídeo
ms.assetid: f0b4f24c-3e35-4a18-ac77-8cae7083b0fe
keywords:
- capDriverGetCaps (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce51a3b7c77fbb161007ddde7dfe91c36152121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779141"
---
# <a name="enabling-video-overlay"></a>Habilitación de la superposición de vídeo

En el ejemplo siguiente se usa la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) para determinar si un controlador de captura tiene capacidades de superposición; Si es así, la macro habilita la superposición.


```C++
CAPDRIVERCAPS CapDrvCaps; 

capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 

if (CapDrvCaps.fHasOverlay) 
    capOverlay(hWndC, TRUE);
 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




