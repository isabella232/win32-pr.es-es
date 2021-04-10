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
# <a name="animationoptions"></a><span data-ttu-id="fddaa-103">AnimationOptions</span><span class="sxs-lookup"><span data-stu-id="fddaa-103">AnimationOptions</span></span>

<span data-ttu-id="fddaa-104">Permite establecer las opciones de animación.</span><span class="sxs-lookup"><span data-stu-id="fddaa-104">Enables you to set animation options.</span></span>

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

<span data-ttu-id="fddaa-105">Donde:</span><span class="sxs-lookup"><span data-stu-id="fddaa-105">Where:</span></span>

-   <span data-ttu-id="fddaa-106">openclosed: Use 0 para una animación cerrada o 1 para una animación abierta.</span><span class="sxs-lookup"><span data-stu-id="fddaa-106">openclosed - Use 0 for a closed animation, or 1 for an open animation.</span></span> <span data-ttu-id="fddaa-107">De forma predeterminada, se cierra una animación.</span><span class="sxs-lookup"><span data-stu-id="fddaa-107">By default, an animation is closed.</span></span>
-   <span data-ttu-id="fddaa-108">positionquality: establece la calidad de la posición para cualquier clave de posición especificada.</span><span class="sxs-lookup"><span data-stu-id="fddaa-108">positionquality - Set the position quality for any position keys specified.</span></span> <span data-ttu-id="fddaa-109">Use 0 para las posiciones de spline o 1 para las posiciones lineales.</span><span class="sxs-lookup"><span data-stu-id="fddaa-109">Use 0 for spline positions or 1 for linear positions.</span></span>

## <a name="see-also"></a><span data-ttu-id="fddaa-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="fddaa-110">See also</span></span>

<dl> <dt>

<span data-ttu-id="fddaa-111">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="fddaa-111">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



