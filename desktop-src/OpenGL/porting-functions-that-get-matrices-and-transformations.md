---
title: Portabilidad de funciones que obtienen matrices y transformaciones
description: En la tabla siguiente se enumeran las funciones de contabilidad de IRIS que obtienen el estado de las matrices y transformaciones y sus equivalentes de OpenGL.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- Puerto de GL de IRIS, matrices
- portabilidad de IRIS GL, matrices
- trasladar a OpenGL desde IRIS GL, matrices
- Exportación de OpenGL desde IRIS GL, matrices
- matrices
- Migración de la contabilidad de IRIS, transformaciones
- portabilidad de IRIS GL, transformaciones
- trasladar a OpenGL desde IRIS GL, transformaciones
- Exportación de OpenGL desde IRIS GL, transformaciones
- transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994334"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a><span data-ttu-id="a4e0b-113">Portabilidad de funciones que obtienen matrices y transformaciones</span><span class="sxs-lookup"><span data-stu-id="a4e0b-113">Porting Functions that Get Matrices and Transformations</span></span>

<span data-ttu-id="a4e0b-114">En la tabla siguiente se enumeran las funciones de contabilidad de IRIS que obtienen el estado de las matrices y transformaciones y sus equivalentes de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-114">The following table lists the IRIS GL functions that get the state of matrices and transformations and their OpenGL equivalents.</span></span>



| <span data-ttu-id="a4e0b-115">Consulta de matriz de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="a4e0b-115">IRIS GL matrix query</span></span>                  | <span data-ttu-id="a4e0b-116">Consulta de matriz OpenGL glGet</span><span class="sxs-lookup"><span data-stu-id="a4e0b-116">OpenGL glGet matrix query</span></span>         | <span data-ttu-id="a4e0b-117">Significado</span><span class="sxs-lookup"><span data-stu-id="a4e0b-117">Meaning</span></span>                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="a4e0b-118">**getmmode**</span><span class="sxs-lookup"><span data-stu-id="a4e0b-118">**getmmode**</span></span>                          | <span data-ttu-id="a4e0b-119">\_modo de matriz de contabilidad general \_</span><span class="sxs-lookup"><span data-stu-id="a4e0b-119">GL\_MATRIX\_MODE</span></span>                  | <span data-ttu-id="a4e0b-120">Devuelve el modo de matriz actual.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-120">Returns the current matrix mode.</span></span>                                |
| <span data-ttu-id="a4e0b-121">**getmatrix** en modo **MVIEWING**</span><span class="sxs-lookup"><span data-stu-id="a4e0b-121">**getmatrix** in **MVIEWING** mode</span></span>    | <span data-ttu-id="a4e0b-122">\_matriz MODELVIEW de GL \_</span><span class="sxs-lookup"><span data-stu-id="a4e0b-122">GL\_MODELVIEW\_MATRIX</span></span>             | <span data-ttu-id="a4e0b-123">Devuelve una copia de la matriz de vista de modelo actual.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-123">Returns a copy of the current model-view matrix.</span></span>                |
| <span data-ttu-id="a4e0b-124">**getmatrix** en modo **MPROJECTION**</span><span class="sxs-lookup"><span data-stu-id="a4e0b-124">**getmatrix** in **MPROJECTION** mode</span></span> | <span data-ttu-id="a4e0b-125">\_matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="a4e0b-125">GL\_PROJECTION\_MATRIX</span></span>            | <span data-ttu-id="a4e0b-126">Devuelve una copia de la matriz de proyección actual.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-126">Returns a copy of the current projection matrix.</span></span>                |
| <span data-ttu-id="a4e0b-127">**getmatrix** en modo **MTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="a4e0b-127">**getmatrix** in **MTEXTURE** mode</span></span>    | <span data-ttu-id="a4e0b-128">\_matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="a4e0b-128">GL\_TEXTURE\_MATRIX</span></span>               | <span data-ttu-id="a4e0b-129">Devuelve una copia de la matriz de textura actual.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-129">Returns a copy of the current texture matrix.</span></span>                   |
| <span data-ttu-id="a4e0b-130">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-130">Not applicable.</span></span>                       | <span data-ttu-id="a4e0b-131">\_profundidad máxima de la \_ \_ pila MODELVIEW \_ de GL</span><span class="sxs-lookup"><span data-stu-id="a4e0b-131">GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>  | <span data-ttu-id="a4e0b-132">Devuelve la profundidad máxima admitida de la pila de matrices de la vista de modelo.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-132">Returns maximum supported depth of the model-view matrix stack.</span></span> |
| <span data-ttu-id="a4e0b-133">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-133">Not applicable.</span></span>                       | <span data-ttu-id="a4e0b-134">\_profundidad máxima de la \_ pila de proyección de \_ GL \_</span><span class="sxs-lookup"><span data-stu-id="a4e0b-134">GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span> | <span data-ttu-id="a4e0b-135">Devuelve la profundidad máxima admitida de la pila de la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-135">Returns maximum supported depth of the projection matrix stack.</span></span> |
| <span data-ttu-id="a4e0b-136">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-136">Not applicable.</span></span>                       | <span data-ttu-id="a4e0b-137">\_profundidad máxima de la \_ pila de textura de \_ GL \_</span><span class="sxs-lookup"><span data-stu-id="a4e0b-137">GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>    | <span data-ttu-id="a4e0b-138">Devuelve la profundidad máxima admitida de la pila de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-138">Returns maximum supported depth of the texture matrix stack.</span></span>    |
| <span data-ttu-id="a4e0b-139">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-139">Not applicable.</span></span>                       | <span data-ttu-id="a4e0b-140">profundidad de la pila de GL \_ MODELVIEW \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4e0b-140">GL\_MODELVIEW\_STACK\_DEPTH</span></span>       | <span data-ttu-id="a4e0b-141">Devuelve el número de matrices en la pila de vistas de modelo.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-141">Returns number of matrices on the model view stack.</span></span>             |
| <span data-ttu-id="a4e0b-142">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-142">Not applicable.</span></span>                       | <span data-ttu-id="a4e0b-143">profundidad de la pila de proyección de contabilidad \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4e0b-143">GL\_PROJECTION\_STACK\_DEPTH</span></span>      | <span data-ttu-id="a4e0b-144">Devuelve el número de matrices en la pila de proyección.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-144">Returns number of matrices on the projection stack.</span></span>             |
| <span data-ttu-id="a4e0b-145">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-145">Not applicable.</span></span>                       | <span data-ttu-id="a4e0b-146">profundidad de la pila de textura de GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a4e0b-146">GL\_TEXTURE\_STACK\_DEPTH</span></span>         | <span data-ttu-id="a4e0b-147">Devuelve el número de matrices de la pila de textura.</span><span class="sxs-lookup"><span data-stu-id="a4e0b-147">Returns number of matrices on the texture stack.</span></span>                |



 

<span data-ttu-id="a4e0b-148">??</span><span class="sxs-lookup"><span data-stu-id="a4e0b-148">??</span></span>

 

 




