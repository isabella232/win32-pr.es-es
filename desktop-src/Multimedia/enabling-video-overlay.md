---
title: Habilitación de la superposición de vídeo
description: Habilitación de la superposición de vídeo
ms.assetid: f0b4f24c-3e35-4a18-ac77-8cae7083b0fe
keywords:
- CapDriverGetCaps macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce51a3b7c77fbb161007ddde7dfe91c36152121
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371371"
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

 

 




