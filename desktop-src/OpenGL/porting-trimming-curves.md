---
title: Trasladar curvas de recorte
description: Las curvas de recorte de OpenGL son muy similares a las curvas de recorte de la contabilidad de IRIS. En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para definir curvas de recorte y sus funciones de OpenGL equivalentes.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Migración de la contabilidad de IRIS, curvas de recorte
- trasladar de IRIS GL, curvas de recorte
- trasladar a OpenGL desde IRIS GL, curvas de recorte
- Exportación de OpenGL desde IRIS GL, curvas de recorte
- curvas de recorte
- curvas
- Migración de la contabilidad de IRIS, curvas
- trasladar de IRIS GL, curvas
- trasladar a OpenGL desde IRIS GL, curvas
- Exportación de OpenGL de IRIS GL, curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269164"
---
# <a name="porting-trimming-curves"></a><span data-ttu-id="6173f-114">Trasladar curvas de recorte</span><span class="sxs-lookup"><span data-stu-id="6173f-114">Porting Trimming Curves</span></span>

<span data-ttu-id="6173f-115">Las curvas de recorte de OpenGL son muy similares a las curvas de recorte de la contabilidad de IRIS.</span><span class="sxs-lookup"><span data-stu-id="6173f-115">OpenGL trimming curves are very similar to IRIS GL trimming curves.</span></span> <span data-ttu-id="6173f-116">En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para definir curvas de recorte y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="6173f-116">The following table lists the IRIS GL functions for defining trimming curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="6173f-117">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="6173f-117">IRIS GL function</span></span> | <span data-ttu-id="6173f-118">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="6173f-118">OpenGL function</span></span>                        | <span data-ttu-id="6173f-119">Significado</span><span class="sxs-lookup"><span data-stu-id="6173f-119">Meaning</span></span>                              |
|------------------|----------------------------------------|--------------------------------------|
| <span data-ttu-id="6173f-120">**bgntrim**</span><span class="sxs-lookup"><span data-stu-id="6173f-120">**bgntrim**</span></span>      | [<span data-ttu-id="6173f-121">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="6173f-121">**gluBeginTrim**</span></span>](glubegintrim.md)   | <span data-ttu-id="6173f-122">Comienza la definición de la curva de recorte.</span><span class="sxs-lookup"><span data-stu-id="6173f-122">Begins trimming-curve definition.</span></span>    |
| <span data-ttu-id="6173f-123">**pwlcurve**</span><span class="sxs-lookup"><span data-stu-id="6173f-123">**pwlcurve**</span></span>     | [<span data-ttu-id="6173f-124">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="6173f-124">**gluPwlCurve**</span></span>](glupwlcurve.md)     | <span data-ttu-id="6173f-125">Define una curva lineal a trozos.</span><span class="sxs-lookup"><span data-stu-id="6173f-125">Defines a piecewise linear curve.</span></span>    |
| <span data-ttu-id="6173f-126">**nurbscurve**</span><span class="sxs-lookup"><span data-stu-id="6173f-126">**nurbscurve**</span></span>   | [<span data-ttu-id="6173f-127">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="6173f-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="6173f-128">Especifica los atributos de curva de recorte.</span><span class="sxs-lookup"><span data-stu-id="6173f-128">Specifies trimming-curve attributes.</span></span> |
| <span data-ttu-id="6173f-129">**endtrim**</span><span class="sxs-lookup"><span data-stu-id="6173f-129">**endtrim**</span></span>      | [<span data-ttu-id="6173f-130">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="6173f-130">**gluEndTrim**</span></span>](gluendtrim.md)       | <span data-ttu-id="6173f-131">Finaliza la definición de curva de recorte.</span><span class="sxs-lookup"><span data-stu-id="6173f-131">Ends trimming-curve definition.</span></span>      |



 

<span data-ttu-id="6173f-132">??</span><span class="sxs-lookup"><span data-stu-id="6173f-132">??</span></span>

 

 




