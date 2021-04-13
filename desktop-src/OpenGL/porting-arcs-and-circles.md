---
title: Trasladar arcos y círculos
description: Con OpenGL, los arcos y los círculos rellenos se dibujan con las mismas llamadas que los arcos y círculos sin rellenar. En la tabla siguiente se enumeran las funciones de arco y círculo de la contabilidad de IRIS y sus funciones de OpenGL (GLU) equivalentes.
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- Migración de la contabilidad de IRIS, arcos
- portabilidad de IRIS GL, arcos
- trasladar a OpenGL desde IRIS GL, arcos
- Exportación de OpenGL desde IRIS GL, arcos
- funciones de dibujo, arcos
- Migración de la contabilidad de IRIS, círculos
- portabilidad de IRIS GL, círculos
- trasladar a OpenGL desde IRIS GL, círculos
- Exportación de OpenGL desde IRIS GL, círculos
- dibujar funciones, círculos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419127"
---
# <a name="porting-arcs-and-circles"></a><span data-ttu-id="31899-114">Trasladar arcos y círculos</span><span class="sxs-lookup"><span data-stu-id="31899-114">Porting Arcs and Circles</span></span>

<span data-ttu-id="31899-115">Con OpenGL, los arcos y los círculos rellenos se dibujan con las mismas llamadas que los arcos y círculos sin rellenar.</span><span class="sxs-lookup"><span data-stu-id="31899-115">With OpenGL, filled arcs and circles are drawn with the same calls as unfilled arcs and circles.</span></span> <span data-ttu-id="31899-116">En la tabla siguiente se enumeran las funciones de arco y círculo de la contabilidad de IRIS y sus funciones de OpenGL (GLU) equivalentes.</span><span class="sxs-lookup"><span data-stu-id="31899-116">The following table lists the IRIS GL arc and circle functions and their equivalent OpenGL (GLU) functions.</span></span>



| <span data-ttu-id="31899-117">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="31899-117">IRIS GL function</span></span> | <span data-ttu-id="31899-118">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="31899-118">OpenGL function</span></span>                          | <span data-ttu-id="31899-119">Significado</span><span class="sxs-lookup"><span data-stu-id="31899-119">Meaning</span></span>                 |
|------------------|------------------------------------------|-------------------------|
| <span data-ttu-id="31899-120">**arcarcf**</span><span class="sxs-lookup"><span data-stu-id="31899-120">**arcarcf**</span></span>      | [<span data-ttu-id="31899-121">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="31899-121">**gluPartialDisk**</span></span>](glupartialdisk.md) | <span data-ttu-id="31899-122">Dibuja un arco.</span><span class="sxs-lookup"><span data-stu-id="31899-122">Draws an arc.</span></span>           |
| <span data-ttu-id="31899-123">**circcircf**</span><span class="sxs-lookup"><span data-stu-id="31899-123">**circcircf**</span></span>    | [<span data-ttu-id="31899-124">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="31899-124">**gluDisk**</span></span>](gludisk.md)               | <span data-ttu-id="31899-125">Dibuja un círculo o un disco.</span><span class="sxs-lookup"><span data-stu-id="31899-125">Draws a circle or disk.</span></span> |



 

<span data-ttu-id="31899-126">Puede hacer algunas cosas con los arcos de OpenGL y los círculos que no se pueden realizar con la contabilidad de IRIS.</span><span class="sxs-lookup"><span data-stu-id="31899-126">You can do some things with OpenGL arcs and circles that you can't do with IRIS GL.</span></span> <span data-ttu-id="31899-127">OpenGL llama a arcos y círculos, discos y discos parciales, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="31899-127">OpenGL calls arcs and circles, disks and partial disks respectively.</span></span>

<span data-ttu-id="31899-128">Al migrar arcos y círculos, tenga en cuenta los siguientes puntos sobre OpenGL:</span><span class="sxs-lookup"><span data-stu-id="31899-128">When porting arcs and circles, keep the following points about OpenGL in mind:</span></span>

-   <span data-ttu-id="31899-129">Los ángulos se miden en grados y no en décimas de grado.</span><span class="sxs-lookup"><span data-stu-id="31899-129">Angles are measured in degrees, and not in tenths of degrees.</span></span>
-   <span data-ttu-id="31899-130">El ángulo inicial se mide desde el eje y positivo y no desde el eje x.</span><span class="sxs-lookup"><span data-stu-id="31899-130">The start angle is measured from the positive y-axis, and not from the x-axis.</span></span>
-   <span data-ttu-id="31899-131">El ángulo de barrido es ahora en lugar de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="31899-131">The sweep angle is now clockwise instead of counterclockwise.</span></span>

<span data-ttu-id="31899-132">??</span><span class="sxs-lookup"><span data-stu-id="31899-132">??</span></span>

 

 




