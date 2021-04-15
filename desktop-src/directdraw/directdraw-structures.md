---
title: Estructuras de DirectDraw
description: Esta sección contiene información acerca de las siguientes estructuras utilizadas con DirectDraw
ms.assetid: 36424B41-B179-414A-ACFF-E63DA7B27043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52cf24c71da3f022833c6ecf9843e996df2c514b
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "105695804"
---
# <a name="directdraw-structures"></a>Estructuras de DirectDraw

Esta sección contiene información acerca de las siguientes estructuras utilizadas con DirectDraw:

-   [**DDBLTBATCH**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltbatch)
-   [**DDBLTFX**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltfx)
-   [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)
-   [**DDCOLORCONTROL**](/windows/win32/api/ddraw/nn-ddraw-idirectdrawcolorcontrol)
-   [**DDCOLORKEY**](/windows/desktop/api/Ddraw/ns-ddraw-ddcolorkey)
-   [**DDDEVICEIDENTIFIER2**](/windows/win32/api/ddraw/ns-ddraw-dddeviceidentifier2)
-   [**DDGAMMARAMP**](/windows/desktop/api/Ddraw/ns-ddraw-ddgammaramp)
-   [**DDOVERLAYFX**](/windows/desktop/api/Ddraw/ns-ddraw-ddoverlayfx)
-   [**DDPIXELFORMAT**](/windows/desktop/api/Ddraw/ns-ddraw-ddpixelformat)
-   [**DDSCAPS**](/previous-versions/ms783271(v=vs.85))
-   [**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))
-   [**DDSURFACEDESC**](/previous-versions/ms783272(v=vs.85))
-   [**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))

> [!Note]  
> Debe inicializar la memoria de cada estructura de DirectX en 0 antes de utilizar la estructura. Además, para todas las estructuras que contienen un miembro **dwSize** , debe establecer el miembro en el tamaño de la estructura, en bytes, antes de que se use la estructura. En el ejemplo siguiente se realizan estas tareas en una estructura común, [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3):

 


```
DDCAPS ddcaps; // You cannot use this yet.
 
ZeroMemory(&ddcaps, sizeof(DDCAPS));
ddcaps.dwSize = sizeof(DDCAPS);
 
// Now you can use the structure.
.
.
```



 

 




