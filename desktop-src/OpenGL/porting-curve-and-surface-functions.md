---
title: Trasladar funciones de curva y superficie
description: Trasladar funciones de curva y superficie
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- Migración de la contabilidad de IRIS, curvas
- trasladar de IRIS GL, curvas
- trasladar a OpenGL desde IRIS GL, curvas
- Exportación de OpenGL de IRIS GL, curvas
- Migración de la contabilidad de IRIS, revisiones de Surface
- portabilidad desde IRIS GL, revisiones de Surface
- trasladar a OpenGL desde IRIS GL, Surface patchs
- Exportación de OpenGL desde IRIS GL, revisiones de Surface
- curvas
- revisiones de Surface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356810"
---
# <a name="porting-curve-and-surface-functions"></a><span data-ttu-id="2c602-113">Trasladar funciones de curva y superficie</span><span class="sxs-lookup"><span data-stu-id="2c602-113">Porting Curve and Surface Functions</span></span>

<span data-ttu-id="2c602-114">OpenGL no admite equivalentes a las funciones de GL de IRIS para curvas y revisiones de superficie.</span><span class="sxs-lookup"><span data-stu-id="2c602-114">OpenGL doesn't support equivalents to the IRIS GL functions for curves and surface patches.</span></span> <span data-ttu-id="2c602-115">Tendrá que volver a escribir el código si incluye cualquiera de las siguientes llamadas:</span><span class="sxs-lookup"><span data-stu-id="2c602-115">You'll need to rewrite your code if it includes any of the following calls:</span></span>

-   <span data-ttu-id="2c602-116">**defbasis**</span><span class="sxs-lookup"><span data-stu-id="2c602-116">**defbasis**</span></span>
-   <span data-ttu-id="2c602-117">**curvebasis**, **curveprecision**, **CRV**, **crvn**, **rcrv**, **rcrvn** y **curveit**</span><span class="sxs-lookup"><span data-stu-id="2c602-117">**curvebasis**, **curveprecision**, **crv**, **crvn**, **rcrv**, **rcrvn**, and **curveit**</span></span>
-   <span data-ttu-id="2c602-118">**patchbasis**, **patchcurves**, **patchprecision**, **patch** y **rpatch**</span><span class="sxs-lookup"><span data-stu-id="2c602-118">**patchbasis**, **patchcurves**, **patchprecision**, **patch**, and **rpatch**</span></span>

<span data-ttu-id="2c602-119">En este tema se incluye información sobre lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="2c602-119">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="2c602-120">Trasladar objetos de NURBS</span><span class="sxs-lookup"><span data-stu-id="2c602-120">Porting NURBS Objects</span></span>](porting-nurbs-objects.md)
-   [<span data-ttu-id="2c602-121">Trasladar curvas de NURBS</span><span class="sxs-lookup"><span data-stu-id="2c602-121">Porting NURBS Curves</span></span>](porting-nurbs-curves.md)
-   [<span data-ttu-id="2c602-122">Trasladar curvas de recorte</span><span class="sxs-lookup"><span data-stu-id="2c602-122">Porting Trimming Curves</span></span>](porting-trimming-curves.md)
-   [<span data-ttu-id="2c602-123">Trasladar superficies NURBS</span><span class="sxs-lookup"><span data-stu-id="2c602-123">Porting NURBS Surfaces</span></span>](porting-nurbs-surfaces.md)

 

 




