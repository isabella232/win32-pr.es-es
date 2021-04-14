---
title: Trasladar funciones de picking
description: Todas las funciones de selección de la contabilidad de IRIS tienen equivalentes de OpenGL, con la excepción de clearhitcode. En la tabla siguiente se enumeran las funciones de picking de IRIS GL y sus funciones de OpenGL equivalentes.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Migración de la contabilidad de IRIS, picking
- portabilidad de IRIS GL, picking
- trasladar a OpenGL desde IRIS GL, picking
- Exportación de OpenGL desde IRIS GL, picking
- recogida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665693"
---
# <a name="porting-picking-functions"></a><span data-ttu-id="8b8d6-109">Trasladar funciones de picking</span><span class="sxs-lookup"><span data-stu-id="8b8d6-109">Porting Picking Functions</span></span>

<span data-ttu-id="8b8d6-110">Todas las funciones de selección de la contabilidad de IRIS tienen equivalentes de OpenGL, con la excepción de **clearhitcode**.</span><span class="sxs-lookup"><span data-stu-id="8b8d6-110">All IRIS GL picking functions have OpenGL equivalents, with the exception of **clearhitcode**.</span></span> <span data-ttu-id="8b8d6-111">En la tabla siguiente se enumeran las funciones de picking de IRIS GL y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="8b8d6-111">The following table lists the IRIS GL picking functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="8b8d6-112">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="8b8d6-112">IRIS GL function</span></span>                | <span data-ttu-id="8b8d6-113">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="8b8d6-113">OpenGL function</span></span>                                                                           | <span data-ttu-id="8b8d6-114">Significado</span><span class="sxs-lookup"><span data-stu-id="8b8d6-114">Meaning</span></span>                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="8b8d6-115">**clearhitcode**</span><span class="sxs-lookup"><span data-stu-id="8b8d6-115">**clearhitcode**</span></span>                | <span data-ttu-id="8b8d6-116">No se admite.</span><span class="sxs-lookup"><span data-stu-id="8b8d6-116">Not supported.</span></span>                                                                            | <span data-ttu-id="8b8d6-117">Borra la variable global y hitcode.</span><span class="sxs-lookup"><span data-stu-id="8b8d6-117">Clears global variable and hitcode.</span></span>    |
| <span data-ttu-id="8b8d6-118">**pickselect**</span><span class="sxs-lookup"><span data-stu-id="8b8d6-118">**pickselect**</span></span><br/>       | <span data-ttu-id="8b8d6-119">[**glRenderMode**](glrendermode.md) (selección de libro \_ )</span><span class="sxs-lookup"><span data-stu-id="8b8d6-119">[**glRenderMode**](glrendermode.md) ( GL\_SELECT )</span></span>                                       | <span data-ttu-id="8b8d6-120">Cambia a la selección o al modo de selección.</span><span class="sxs-lookup"><span data-stu-id="8b8d6-120">Switches to selection or picking mode.</span></span> |
| <span data-ttu-id="8b8d6-121">**endpickendselect**</span><span class="sxs-lookup"><span data-stu-id="8b8d6-121">**endpickendselect**</span></span><br/> | <span data-ttu-id="8b8d6-122">[**glRenderMode**](glrendermode.md) (representación en GL \_ )</span><span class="sxs-lookup"><span data-stu-id="8b8d6-122">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )</span></span>                                       | <span data-ttu-id="8b8d6-123">Cambia al modo de representación.</span><span class="sxs-lookup"><span data-stu-id="8b8d6-123">Switches to rendering mode.</span></span>            |
| <span data-ttu-id="8b8d6-124">**picksize**</span><span class="sxs-lookup"><span data-stu-id="8b8d6-124">**picksize**</span></span>                    | <span data-ttu-id="8b8d6-125">[**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="8b8d6-125">[**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)</span></span><br/> | <span data-ttu-id="8b8d6-126">Establece la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="8b8d6-126">Sets the return array.</span></span>                 |
| <span data-ttu-id="8b8d6-127">**initnames**</span><span class="sxs-lookup"><span data-stu-id="8b8d6-127">**initnames**</span></span>                   | [<span data-ttu-id="8b8d6-128">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="8b8d6-128">**glInitNames**</span></span>](glinitnames.md)                                                        |                                        |
| <span data-ttu-id="8b8d6-129">**pushnamepopname**</span><span class="sxs-lookup"><span data-stu-id="8b8d6-129">**pushnamepopname**</span></span><br/>  | <span data-ttu-id="8b8d6-130">[**glPushName**](glpushname.md)[**glPopName**](glpopname.md)</span><span class="sxs-lookup"><span data-stu-id="8b8d6-130">[**glPushName**](glpushname.md)[**glPopName**](glpopname.md)</span></span><br/>                 |                                        |
| <span data-ttu-id="8b8d6-131">**loadname**</span><span class="sxs-lookup"><span data-stu-id="8b8d6-131">**loadname**</span></span>                    | [<span data-ttu-id="8b8d6-132">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="8b8d6-132">**glLoadName**</span></span>](glloadname.md)                                                          |                                        |



 

<span data-ttu-id="8b8d6-133">Para obtener más información sobre la selección, vea [**gluPickMatrix**](glupickmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="8b8d6-133">For more information on picking, see [**gluPickMatrix**](glupickmatrix.md).</span></span>

 

 





