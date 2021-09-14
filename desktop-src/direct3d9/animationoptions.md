---
description: Permite establecer opciones de animación.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd3c5df8081523ccef2a802e631454fadaeeae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060773"
---
# <a name="animationoptions"></a>AnimationOptions

Permite establecer opciones de animación.

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

Donde:

-   openclosed: use 0 para una animación cerrada o 1 para una animación abierta. De forma predeterminada, se cierra una animación.
-   positionquality: establezca la calidad de la posición para las claves de posición especificadas. Use 0 para las posiciones spline o 1 para las posiciones lineales.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



