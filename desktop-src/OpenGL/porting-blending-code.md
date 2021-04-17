---
title: Trasladar código de fusión
description: En la contabilidad de IRIS, al dibujar en los búferes frontal y posterior, la combinación se realiza mediante la lectura de uno de los búferes, la fusión con ese color y la posterior escritura del resultado en ambos búferes. En OpenGL, sin embargo, cada búfer se lee a su vez, se mezcla y se escribe.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- Migración de la contabilidad de IRIS, fusión
- portabilidad de IRIS GL, fusión
- trasladar a OpenGL desde IRIS GL, fusión
- Exportación de OpenGL desde IRIS GL, fusión
- combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665719"
---
# <a name="porting-blending-code"></a><span data-ttu-id="07019-109">Trasladar código de fusión</span><span class="sxs-lookup"><span data-stu-id="07019-109">Porting Blending Code</span></span>

<span data-ttu-id="07019-110">En la contabilidad de IRIS, al dibujar en los búferes frontal y posterior, la combinación se realiza mediante la lectura de uno de los búferes, la fusión con ese color y la posterior escritura del resultado en ambos búferes.</span><span class="sxs-lookup"><span data-stu-id="07019-110">In IRIS GL, when drawing to both front and back buffers, blending is done by reading one of the buffers, blending with that color, and then writing the result to both buffers.</span></span> <span data-ttu-id="07019-111">En OpenGL, sin embargo, cada búfer se lee a su vez, se mezcla y se escribe.</span><span class="sxs-lookup"><span data-stu-id="07019-111">In OpenGL, however, each buffer is read in turn, blended, and then written.</span></span>

<span data-ttu-id="07019-112">En la tabla siguiente se enumeran las funciones de fusión en GL de IRIS y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="07019-112">The following table lists IRIS GL blending functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="07019-113">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="07019-113">IRIS GL function</span></span>  | <span data-ttu-id="07019-114">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="07019-114">OpenGL function</span></span>                            | <span data-ttu-id="07019-115">Significado</span><span class="sxs-lookup"><span data-stu-id="07019-115">Meaning</span></span>                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | <span data-ttu-id="07019-116">[**glEnable**](glenable.md) (GL \_ Blend)</span><span class="sxs-lookup"><span data-stu-id="07019-116">[**glEnable**](glenable.md) ( GL\_BLEND )</span></span> | <span data-ttu-id="07019-117">Activa la fusión.</span><span class="sxs-lookup"><span data-stu-id="07019-117">Turns on blending.</span></span>          |
| <span data-ttu-id="07019-118">**blendfunction**</span><span class="sxs-lookup"><span data-stu-id="07019-118">**blendfunction**</span></span> | [<span data-ttu-id="07019-119">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="07019-119">**glBlendFunc**</span></span>](glblendfunc.md)         | <span data-ttu-id="07019-120">Especifica una función de Blend.</span><span class="sxs-lookup"><span data-stu-id="07019-120">Specifies a blend function.</span></span> |



 

<span data-ttu-id="07019-121">La función **glBlendFunc** de OpenGL y la función **BLENDFUNCTION** de la contabilidad de iris son casi idénticas.</span><span class="sxs-lookup"><span data-stu-id="07019-121">The OpenGL **glBlendFunc** function and the IRIS GL **blendfunction** function are almost identical.</span></span> <span data-ttu-id="07019-122">En la tabla siguiente se enumeran los factores de mezcla de IRIS GL y sus equivalentes de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="07019-122">The following table lists IRIS GL blend factors and their OpenGL equivalents.</span></span>



| <span data-ttu-id="07019-123">IRIS GL</span><span class="sxs-lookup"><span data-stu-id="07019-123">IRIS GL</span></span>          | <span data-ttu-id="07019-124">OpenGL</span><span class="sxs-lookup"><span data-stu-id="07019-124">OpenGL</span></span>                     | <span data-ttu-id="07019-125">Notas</span><span class="sxs-lookup"><span data-stu-id="07019-125">Notes</span></span>             |
|------------------|----------------------------|-------------------|
| <span data-ttu-id="07019-126">BF \_ cero</span><span class="sxs-lookup"><span data-stu-id="07019-126">BF\_ZERO</span></span>         | <span data-ttu-id="07019-127">GL \_ cero</span><span class="sxs-lookup"><span data-stu-id="07019-127">GL\_ZERO</span></span>                   |                   |
| <span data-ttu-id="07019-128">BF \_ uno</span><span class="sxs-lookup"><span data-stu-id="07019-128">BF\_ONE</span></span>          | <span data-ttu-id="07019-129">GL \_ uno</span><span class="sxs-lookup"><span data-stu-id="07019-129">GL\_ONE</span></span>                    |                   |
| <span data-ttu-id="07019-130">SA de BF \_</span><span class="sxs-lookup"><span data-stu-id="07019-130">BF\_SA</span></span>           | <span data-ttu-id="07019-131">CC \_ src \_ alfa</span><span class="sxs-lookup"><span data-stu-id="07019-131">GL\_SRC\_ALPHA</span></span>             |                   |
| <span data-ttu-id="07019-132">BF \_ MSA</span><span class="sxs-lookup"><span data-stu-id="07019-132">BF\_MSA</span></span>          | <span data-ttu-id="07019-133">GL \_ uno \_ menos \_ src \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="07019-133">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> |                   |
| <span data-ttu-id="07019-134">BF \_ da</span><span class="sxs-lookup"><span data-stu-id="07019-134">BF\_DA</span></span>           | <span data-ttu-id="07019-135">GL \_ DST \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="07019-135">GL\_DST\_ALPHA</span></span>             |                   |
| <span data-ttu-id="07019-136">MDA de BF \_</span><span class="sxs-lookup"><span data-stu-id="07019-136">BF\_MDA</span></span>          | <span data-ttu-id="07019-137">GL \_ uno \_ menos \_ DST \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="07019-137">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> |                   |
| <span data-ttu-id="07019-138">BF \_ SC</span><span class="sxs-lookup"><span data-stu-id="07019-138">BF\_SC</span></span>           | <span data-ttu-id="07019-139">\_color de origen del libro de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="07019-139">GL\_SRC\_COLOR</span></span>             |                   |
| <span data-ttu-id="07019-140">BF \_ MSC</span><span class="sxs-lookup"><span data-stu-id="07019-140">BF\_MSC</span></span>          | <span data-ttu-id="07019-141">GL \_ uno \_ menos \_ el \_ color src</span><span class="sxs-lookup"><span data-stu-id="07019-141">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="07019-142">Solo destino.</span><span class="sxs-lookup"><span data-stu-id="07019-142">Destination only.</span></span> |
| <span data-ttu-id="07019-143">BF \_ DC</span><span class="sxs-lookup"><span data-stu-id="07019-143">BF\_DC</span></span>           | <span data-ttu-id="07019-144">\_color de DST de GL \_</span><span class="sxs-lookup"><span data-stu-id="07019-144">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="07019-145">Solo origen.</span><span class="sxs-lookup"><span data-stu-id="07019-145">Source only.</span></span>      |
| <span data-ttu-id="07019-146">MDC de BF \_</span><span class="sxs-lookup"><span data-stu-id="07019-146">BF\_MDC</span></span>          | <span data-ttu-id="07019-147">GL \_ uno \_ menos \_ el \_ color de DST</span><span class="sxs-lookup"><span data-stu-id="07019-147">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="07019-148">Solo origen.</span><span class="sxs-lookup"><span data-stu-id="07019-148">Source only.</span></span>      |
| <span data-ttu-id="07019-149">\_MDA del mínimo \_ SA \_ de BF</span><span class="sxs-lookup"><span data-stu-id="07019-149">BF\_MIN\_SA\_MDA</span></span> | <span data-ttu-id="07019-150">libro de contabilidad \_ orig \_ alfa \_ saturado</span><span class="sxs-lookup"><span data-stu-id="07019-150">GL\_SRC\_ALPHA\_SATURATE</span></span>   |                   |



 

<span data-ttu-id="07019-151">??</span><span class="sxs-lookup"><span data-stu-id="07019-151">??</span></span>

 

 




