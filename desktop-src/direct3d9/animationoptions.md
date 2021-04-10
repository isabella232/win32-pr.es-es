---
description: Permite establecer las opciones de animación.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd3c5df8081523ccef2a802e631454fadaeeae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153252"
---
# <a name="animationoptions"></a>AnimationOptions

Permite establecer las opciones de animación.

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

Donde:

-   openclosed: Use 0 para una animación cerrada o 1 para una animación abierta. De forma predeterminada, se cierra una animación.
-   positionquality: establece la calidad de la posición para cualquier clave de posición especificada. Use 0 para las posiciones de spline o 1 para las posiciones lineales.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



