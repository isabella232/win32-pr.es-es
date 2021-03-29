---
title: Trasladar los planos de recorte
description: OpenGL implementa los planos de recorte de forma similar a IRIS GL. Además, en OpenGL puede consultar los planos de recorte. En la tabla siguiente se enumeran las funciones de plano de recorte del IRIS GL y sus funciones de OpenGL equivalentes.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- Migración de GL de IRIS, planos de recorte
- portabilidad de IRIS GL, planos de recorte
- portabilidad a OpenGL desde IRIS GL, planos de recorte
- Exportación de OpenGL desde IRIS GL, planos de recorte
- planos de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b531b39daf6670a3a99d9a4cbcf55158ea2d4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779117"
---
# <a name="porting-clipping-planes"></a><span data-ttu-id="d4347-110">Trasladar los planos de recorte</span><span class="sxs-lookup"><span data-stu-id="d4347-110">Porting Clipping Planes</span></span>

<span data-ttu-id="d4347-111">OpenGL implementa los planos de recorte de forma similar a IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="d4347-111">OpenGL implements clipping planes similarly to IRIS GL.</span></span> <span data-ttu-id="d4347-112">Además, en OpenGL puede consultar los planos de recorte.</span><span class="sxs-lookup"><span data-stu-id="d4347-112">In addition, in OpenGL you can query clipping planes.</span></span> <span data-ttu-id="d4347-113">En la tabla siguiente se enumeran las funciones de plano de recorte del IRIS GL y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="d4347-113">The following table lists IRIS GL clipping plane functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="d4347-114">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="d4347-114">IRIS GL function</span></span>                          | <span data-ttu-id="d4347-115">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="d4347-115">OpenGL function</span></span>                                                                               | <span data-ttu-id="d4347-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d4347-116">Meaning</span></span>                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="d4347-117">**clipplane** (i, **CP \_ on**, params)</span><span class="sxs-lookup"><span data-stu-id="d4347-117">**clipplane** (i, **CP\_ON**, params)</span></span>     | <span data-ttu-id="d4347-118">[**glEnable**](glenable.md) (plano de clip de contabilidad \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="d4347-118">[**glEnable**](glenable.md) ( GL\_CLIP\_PLANEi )</span></span>                                             | <span data-ttu-id="d4347-119">Habilita el recorte en el plano i.</span><span class="sxs-lookup"><span data-stu-id="d4347-119">Enables clipping on plane i.</span></span>             |
| <span data-ttu-id="d4347-120">**clipplane**(i, **\_ definición de CP**, plano)</span><span class="sxs-lookup"><span data-stu-id="d4347-120">**clipplane**( i, **CP\_DEFINE**, plane )</span></span> | <span data-ttu-id="d4347-121">[**glClipPlane**](glclipplane.md) ( \_ \_ plano de clip de contabilidad general, plano)</span><span class="sxs-lookup"><span data-stu-id="d4347-121">[**glClipPlane**](glclipplane.md) ( GL\_CLIP\_PLANEi, plane )</span></span>                                | <span data-ttu-id="d4347-122">Define el plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="d4347-122">Defines clipping plane.</span></span>                  |
|                                           | [<span data-ttu-id="d4347-123">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="d4347-123">**glGetClipPlane**</span></span>](glgetclipplane.md)                                                      | <span data-ttu-id="d4347-124">Devuelve la ecuación del plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="d4347-124">Returns clipping plane equation.</span></span>         |
|                                           | <span data-ttu-id="d4347-125">[**glIsEnabled**](glisenabled.md) (plano de clip de contabilidad \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="d4347-125">[**glIsEnabled**](glisenabled.md) ( GL\_CLIP\_PLANEi )</span></span>                                       | <span data-ttu-id="d4347-126">Devuelve true si está habilitado el plano de recortes.</span><span class="sxs-lookup"><span data-stu-id="d4347-126">Returns true if clip plane i is enabled.</span></span> |
| <span data-ttu-id="d4347-127">**scrmask**</span><span class="sxs-lookup"><span data-stu-id="d4347-127">**scrmask**</span></span>                               | [<span data-ttu-id="d4347-128">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="d4347-128">**glScissor**</span></span>](glscissor.md)                                                                | <span data-ttu-id="d4347-129">Define el cuadro de tijeras.</span><span class="sxs-lookup"><span data-stu-id="d4347-129">Defines the scissor box.</span></span>                 |
| <span data-ttu-id="d4347-130">**getscrmask**</span><span class="sxs-lookup"><span data-stu-id="d4347-130">**getscrmask**</span></span>                            | <span data-ttu-id="d4347-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ cuadro de tijeras de contabilidad \_ )</span><span class="sxs-lookup"><span data-stu-id="d4347-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SCISSOR\_BOX )</span></span> | <span data-ttu-id="d4347-132">Devuelve el rectángulo de tijeras actual.</span><span class="sxs-lookup"><span data-stu-id="d4347-132">Returns the current scissor box.</span></span>         |



 

<span data-ttu-id="d4347-133">Para activar la prueba de tijeras, llame a **glEnable** con \_ el cuadro con tijeras de GL \_ como parámetro.</span><span class="sxs-lookup"><span data-stu-id="d4347-133">To turn on the scissor test, call **glEnable** using GL\_SCISSOR\_BOX as the parameter.</span></span>

<span data-ttu-id="d4347-134">??</span><span class="sxs-lookup"><span data-stu-id="d4347-134">??</span></span>

 

 




