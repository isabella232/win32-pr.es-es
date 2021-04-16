---
title: Trasladar llamadas de plano de estarcido
description: En OpenGL, se asignan los planos de estarcido solicitando el formato de píxel adecuado con OpenGL auxInitDisplayMode o ChoosePixelFormat.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- Migración de la contabilidad de IRIS, planos de estarcido
- portabilidad de IRIS GL, planos de estarcido
- trasladar a OpenGL desde IRIS GL, planos de estarcido
- Exportación de OpenGL desde IRIS GL, planos de estarcido
- planos de estarcido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357353"
---
# <a name="porting-stencil-plane-calls"></a><span data-ttu-id="74907-108">Trasladar llamadas de plano de estarcido</span><span class="sxs-lookup"><span data-stu-id="74907-108">Porting Stencil Plane Calls</span></span>

<span data-ttu-id="74907-109">En OpenGL, se asignan los planos de estarcido solicitando el formato de píxel adecuado con OpenGL **auxInitDisplayMode** o [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span><span class="sxs-lookup"><span data-stu-id="74907-109">In OpenGL, you allocate stencil planes by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span> <span data-ttu-id="74907-110">dia.</span><span class="sxs-lookup"><span data-stu-id="74907-110">functions.</span></span> <span data-ttu-id="74907-111">En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS que afectan a los planos de estarcido y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="74907-111">The following table lists IRIS GL functions that affect the stencil planes and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="74907-112">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="74907-112">IRIS GL function</span></span>             | <span data-ttu-id="74907-113">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="74907-113">OpenGL function</span></span>                                         | <span data-ttu-id="74907-114">Significado</span><span class="sxs-lookup"><span data-stu-id="74907-114">Meaning</span></span>                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="74907-115">**stensize**</span><span class="sxs-lookup"><span data-stu-id="74907-115">**stensize**</span></span>                 | <span data-ttu-id="74907-116">**ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="74907-116">**ChoosePixelFormat**</span></span>                                   |                                                        |
| <span data-ttu-id="74907-117">**Galería de símbolos**( **true**,...)</span><span class="sxs-lookup"><span data-stu-id="74907-117">**stencil**( **TRUE**, ... )</span></span> | <span data-ttu-id="74907-118">[**glEnable**](glenable.md) (GL \_ stencil \_ Test)</span><span class="sxs-lookup"><span data-stu-id="74907-118">[**glEnable**](glenable.md) ( GL\_STENCIL\_TEST )</span></span>      | <span data-ttu-id="74907-119">Habilita las pruebas de estarcido.</span><span class="sxs-lookup"><span data-stu-id="74907-119">Enables stencil tests.</span></span>                                 |
| <span data-ttu-id="74907-120">**estarcido**</span><span class="sxs-lookup"><span data-stu-id="74907-120">**stencil**</span></span>                  | [<span data-ttu-id="74907-121">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="74907-121">**glStencilOp**</span></span>](glstencilop.md)                      | <span data-ttu-id="74907-122">Establece las acciones de prueba de estarcido.</span><span class="sxs-lookup"><span data-stu-id="74907-122">Sets stencil test actions.</span></span>                             |
| <span data-ttu-id="74907-123">**Galería de símbolos**(... FUNC,...)</span><span class="sxs-lookup"><span data-stu-id="74907-123">**stencil**(... func, ... )</span></span>  | [<span data-ttu-id="74907-124">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="74907-124">**glStencilFunc**</span></span>](glstencilfunc.md)                  | <span data-ttu-id="74907-125">Establece la función y el valor de referencia para las pruebas de estarcido.</span><span class="sxs-lookup"><span data-stu-id="74907-125">Sets function and reference value for stencil testing.</span></span> |
| <span data-ttu-id="74907-126">**swritemask**</span><span class="sxs-lookup"><span data-stu-id="74907-126">**swritemask**</span></span>               | [<span data-ttu-id="74907-127">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="74907-127">**glStencilMask**</span></span>](glstencilmask.md)                  | <span data-ttu-id="74907-128">Especifica los bits de estarcido que se pueden escribir.</span><span class="sxs-lookup"><span data-stu-id="74907-128">Specifies which stencil bits can be written.</span></span>           |
|                              | [<span data-ttu-id="74907-129">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="74907-129">**glClearStencil**</span></span>](glclearstencil.md)                | <span data-ttu-id="74907-130">Especifica el valor sin cifrar para el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="74907-130">Specifies the clear value for the stencil buffer.</span></span>      |
| <span data-ttu-id="74907-131">**sclear**</span><span class="sxs-lookup"><span data-stu-id="74907-131">**sclear**</span></span>                   | <span data-ttu-id="74907-132">[**glClear**](glclear.md) (bit de búfer de estarcido de GL \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="74907-132">[**glClear**](glclear.md) ( GL\_STENCIL\_BUFFER\_BIT )</span></span> |                                                        |



 

<span data-ttu-id="74907-133">Las funciones de comparación de estarcido y las operaciones de conmutación por error y de estarcido son casi equivalentes en OpenGL y IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="74907-133">Stencil-comparison functions and stencil pass/fail operations are nearly equivalent in OpenGL and IRIS GL.</span></span> <span data-ttu-id="74907-134">Las marcas de función de la galería de símbolos GL de IRIS están precedidas por SF; marcas OpenGL con GL.</span><span class="sxs-lookup"><span data-stu-id="74907-134">The IRIS GL stencil-function flags are prefaced with SF; the OpenGL flags with GL.</span></span> <span data-ttu-id="74907-135">Las marcas de la operación Pass/Fail de IRIS se anteponen a ST; marcas OpenGL con GL.</span><span class="sxs-lookup"><span data-stu-id="74907-135">IRIS GL pass/fail operation flags are prefaced with ST; the OpenGL flags with GL.</span></span>

 

 




