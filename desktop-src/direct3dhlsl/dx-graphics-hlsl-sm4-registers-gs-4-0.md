---
title: 'Registros: gs_4_0'
description: Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de geometría versión 4 \_ 0.
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532194"
---
# <a name="registers---gs_4_0"></a><span data-ttu-id="b2435-103">Registros-GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2435-103">Registers - gs\_4\_0</span></span>

<span data-ttu-id="b2435-104">Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de geometría versión 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="b2435-104">This section contains reference information for the input and output registers implemented by geometry shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="b2435-105">Registros de entrada</span><span class="sxs-lookup"><span data-stu-id="b2435-105">Input Registers</span></span>



| <span data-ttu-id="b2435-106">Registrarse</span><span class="sxs-lookup"><span data-stu-id="b2435-106">Register</span></span>                 | <span data-ttu-id="b2435-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="b2435-107">Name</span></span> | <span data-ttu-id="b2435-108">Count</span><span class="sxs-lookup"><span data-stu-id="b2435-108">Count</span></span>              | <span data-ttu-id="b2435-109">L/E</span><span class="sxs-lookup"><span data-stu-id="b2435-109">R/W</span></span> | <span data-ttu-id="b2435-110">Dimensión</span><span class="sxs-lookup"><span data-stu-id="b2435-110">Dimension</span></span>        | <span data-ttu-id="b2435-111">Indexable por r\#</span><span class="sxs-lookup"><span data-stu-id="b2435-111">Indexable by r\#</span></span> | <span data-ttu-id="b2435-112">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="b2435-112">Defaults</span></span> | <span data-ttu-id="b2435-113">Requiere DCL</span><span class="sxs-lookup"><span data-stu-id="b2435-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="b2435-114">c\#</span><span class="sxs-lookup"><span data-stu-id="b2435-114">r\#</span></span>                      |      | <span data-ttu-id="b2435-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="b2435-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="b2435-116">L/E</span><span class="sxs-lookup"><span data-stu-id="b2435-116">R/W</span></span> | <span data-ttu-id="b2435-117">4</span><span class="sxs-lookup"><span data-stu-id="b2435-117">4</span></span>                | <span data-ttu-id="b2435-118">No</span><span class="sxs-lookup"><span data-stu-id="b2435-118">No</span></span>               | <span data-ttu-id="b2435-119">None</span><span class="sxs-lookup"><span data-stu-id="b2435-119">None</span></span>     | <span data-ttu-id="b2435-120">Sí</span><span class="sxs-lookup"><span data-stu-id="b2435-120">Yes</span></span>          |
| <span data-ttu-id="b2435-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="b2435-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="b2435-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="b2435-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="b2435-123">L/E</span><span class="sxs-lookup"><span data-stu-id="b2435-123">R/W</span></span> | <span data-ttu-id="b2435-124">4</span><span class="sxs-lookup"><span data-stu-id="b2435-124">4</span></span>                | <span data-ttu-id="b2435-125">Sí</span><span class="sxs-lookup"><span data-stu-id="b2435-125">Yes</span></span>              | <span data-ttu-id="b2435-126">None</span><span class="sxs-lookup"><span data-stu-id="b2435-126">None</span></span>     | <span data-ttu-id="b2435-127">Sí</span><span class="sxs-lookup"><span data-stu-id="b2435-127">Yes</span></span>          |
| <span data-ttu-id="b2435-128">\# \[ elemento de vértice \] \[ v\]</span><span class="sxs-lookup"><span data-stu-id="b2435-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="b2435-129">32</span><span class="sxs-lookup"><span data-stu-id="b2435-129">32</span></span>                 | <span data-ttu-id="b2435-130">R</span><span class="sxs-lookup"><span data-stu-id="b2435-130">R</span></span>   | <span data-ttu-id="b2435-131">4 (COMP) \* 6 (Vert)</span><span class="sxs-lookup"><span data-stu-id="b2435-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="b2435-132">Sí</span><span class="sxs-lookup"><span data-stu-id="b2435-132">Yes</span></span>              | <span data-ttu-id="b2435-133">None</span><span class="sxs-lookup"><span data-stu-id="b2435-133">None</span></span>     | <span data-ttu-id="b2435-134">Sí</span><span class="sxs-lookup"><span data-stu-id="b2435-134">Yes</span></span>          |
| <span data-ttu-id="b2435-135">vprim</span><span class="sxs-lookup"><span data-stu-id="b2435-135">vprim</span></span>                    |      | <span data-ttu-id="b2435-136">1</span><span class="sxs-lookup"><span data-stu-id="b2435-136">1</span></span>                  | <span data-ttu-id="b2435-137">R</span><span class="sxs-lookup"><span data-stu-id="b2435-137">R</span></span>   | <span data-ttu-id="b2435-138">1</span><span class="sxs-lookup"><span data-stu-id="b2435-138">1</span></span>                | <span data-ttu-id="b2435-139">No</span><span class="sxs-lookup"><span data-stu-id="b2435-139">No</span></span>               | <span data-ttu-id="b2435-140">None</span><span class="sxs-lookup"><span data-stu-id="b2435-140">None</span></span>     | <span data-ttu-id="b2435-141">Sí</span><span class="sxs-lookup"><span data-stu-id="b2435-141">Yes</span></span>          |
| <span data-ttu-id="b2435-142">h\#</span><span class="sxs-lookup"><span data-stu-id="b2435-142">t\#</span></span>                      |      | <span data-ttu-id="b2435-143">128</span><span class="sxs-lookup"><span data-stu-id="b2435-143">128</span></span>                | <span data-ttu-id="b2435-144">R</span><span class="sxs-lookup"><span data-stu-id="b2435-144">R</span></span>   | <span data-ttu-id="b2435-145">1</span><span class="sxs-lookup"><span data-stu-id="b2435-145">1</span></span>                | <span data-ttu-id="b2435-146">No</span><span class="sxs-lookup"><span data-stu-id="b2435-146">No</span></span>               | <span data-ttu-id="b2435-147">None</span><span class="sxs-lookup"><span data-stu-id="b2435-147">None</span></span>     | <span data-ttu-id="b2435-148">Sí</span><span class="sxs-lookup"><span data-stu-id="b2435-148">Yes</span></span>          |
| <span data-ttu-id="b2435-149">s\#</span><span class="sxs-lookup"><span data-stu-id="b2435-149">s\#</span></span>                      |      | <span data-ttu-id="b2435-150">16</span><span class="sxs-lookup"><span data-stu-id="b2435-150">16</span></span>                 | <span data-ttu-id="b2435-151">R</span><span class="sxs-lookup"><span data-stu-id="b2435-151">R</span></span>   | <span data-ttu-id="b2435-152">1</span><span class="sxs-lookup"><span data-stu-id="b2435-152">1</span></span>                | <span data-ttu-id="b2435-153">No</span><span class="sxs-lookup"><span data-stu-id="b2435-153">No</span></span>               | <span data-ttu-id="b2435-154">None</span><span class="sxs-lookup"><span data-stu-id="b2435-154">None</span></span>     | <span data-ttu-id="b2435-155">Sí</span><span class="sxs-lookup"><span data-stu-id="b2435-155">Yes</span></span>          |
| <span data-ttu-id="b2435-156">\# \[ Índice CB\]</span><span class="sxs-lookup"><span data-stu-id="b2435-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="b2435-157">15</span><span class="sxs-lookup"><span data-stu-id="b2435-157">15</span></span>                 | <span data-ttu-id="b2435-158">R</span><span class="sxs-lookup"><span data-stu-id="b2435-158">R</span></span>   | <span data-ttu-id="b2435-159">4</span><span class="sxs-lookup"><span data-stu-id="b2435-159">4</span></span>                | <span data-ttu-id="b2435-160">Sí (contenido)</span><span class="sxs-lookup"><span data-stu-id="b2435-160">Yes(Contents)</span></span>    | <span data-ttu-id="b2435-161">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b2435-161">None</span></span>     | <span data-ttu-id="b2435-162">Sí</span><span class="sxs-lookup"><span data-stu-id="b2435-162">Yes</span></span>          |
| <span data-ttu-id="b2435-163">Índice de ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="b2435-163">icb\[index\]</span></span>             |      | <span data-ttu-id="b2435-164">1</span><span class="sxs-lookup"><span data-stu-id="b2435-164">1</span></span>                  | <span data-ttu-id="b2435-165">R</span><span class="sxs-lookup"><span data-stu-id="b2435-165">R</span></span>   | <span data-ttu-id="b2435-166">4</span><span class="sxs-lookup"><span data-stu-id="b2435-166">4</span></span>                | <span data-ttu-id="b2435-167">Sí (contenido)</span><span class="sxs-lookup"><span data-stu-id="b2435-167">Yes(Contents)</span></span>    | <span data-ttu-id="b2435-168">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b2435-168">None</span></span>     | <span data-ttu-id="b2435-169">Sí</span><span class="sxs-lookup"><span data-stu-id="b2435-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="b2435-170">Registros de salida</span><span class="sxs-lookup"><span data-stu-id="b2435-170">Output Registers</span></span>



| <span data-ttu-id="b2435-171">Registrarse</span><span class="sxs-lookup"><span data-stu-id="b2435-171">Register</span></span> | <span data-ttu-id="b2435-172">Nombre</span><span class="sxs-lookup"><span data-stu-id="b2435-172">Name</span></span>            | <span data-ttu-id="b2435-173">Count</span><span class="sxs-lookup"><span data-stu-id="b2435-173">Count</span></span> | <span data-ttu-id="b2435-174">L/E</span><span class="sxs-lookup"><span data-stu-id="b2435-174">R/W</span></span> | <span data-ttu-id="b2435-175">Dimensión</span><span class="sxs-lookup"><span data-stu-id="b2435-175">Dimension</span></span> | <span data-ttu-id="b2435-176">Indexable por r\#</span><span class="sxs-lookup"><span data-stu-id="b2435-176">Indexable by r\#</span></span> | <span data-ttu-id="b2435-177">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="b2435-177">Defaults</span></span> | <span data-ttu-id="b2435-178">Requiere DCL</span><span class="sxs-lookup"><span data-stu-id="b2435-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="b2435-179">NULL</span><span class="sxs-lookup"><span data-stu-id="b2435-179">NULL</span></span>     | <span data-ttu-id="b2435-180">Descartar resultado</span><span class="sxs-lookup"><span data-stu-id="b2435-180">Discard Result</span></span>  | <span data-ttu-id="b2435-181">N/D</span><span class="sxs-lookup"><span data-stu-id="b2435-181">N/A</span></span>   | <span data-ttu-id="b2435-182">W</span><span class="sxs-lookup"><span data-stu-id="b2435-182">W</span></span>   | <span data-ttu-id="b2435-183">N/D</span><span class="sxs-lookup"><span data-stu-id="b2435-183">N/A</span></span>       | <span data-ttu-id="b2435-184">N/D</span><span class="sxs-lookup"><span data-stu-id="b2435-184">N/A</span></span>              | <span data-ttu-id="b2435-185">N/D</span><span class="sxs-lookup"><span data-stu-id="b2435-185">N/A</span></span>      | <span data-ttu-id="b2435-186">No</span><span class="sxs-lookup"><span data-stu-id="b2435-186">No</span></span>           |
| <span data-ttu-id="b2435-187">aceptar\#</span><span class="sxs-lookup"><span data-stu-id="b2435-187">o\#</span></span>      | <span data-ttu-id="b2435-188">Registro de salida</span><span class="sxs-lookup"><span data-stu-id="b2435-188">Output Register</span></span> | <span data-ttu-id="b2435-189">32</span><span class="sxs-lookup"><span data-stu-id="b2435-189">32</span></span>    | <span data-ttu-id="b2435-190">W</span><span class="sxs-lookup"><span data-stu-id="b2435-190">W</span></span>   | <span data-ttu-id="b2435-191">N/D</span><span class="sxs-lookup"><span data-stu-id="b2435-191">N/A</span></span>       | <span data-ttu-id="b2435-192">N/D</span><span class="sxs-lookup"><span data-stu-id="b2435-192">N/A</span></span>              | <span data-ttu-id="b2435-193">4</span><span class="sxs-lookup"><span data-stu-id="b2435-193">4</span></span>        | <span data-ttu-id="b2435-194">Sí</span><span class="sxs-lookup"><span data-stu-id="b2435-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="b2435-195">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2435-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2435-196">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b2435-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




