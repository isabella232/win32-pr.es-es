---
title: 'Registros: ps_4_0'
description: Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de píxeles versión 4 \_ 0.
ms.assetid: 8b83667f-f599-4105-b68c-0d6aa7c528ab
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3dea9606419f32a168c08cc1efbebb5e285d3815
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418757"
---
# <a name="registers---ps_4_0"></a><span data-ttu-id="8524c-103">Registros: PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8524c-103">Registers - ps\_4\_0</span></span>

<span data-ttu-id="8524c-104">Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de píxeles versión 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="8524c-104">This section contains reference information for the input and output registers implemented by pixel shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="8524c-105">Registros de entrada</span><span class="sxs-lookup"><span data-stu-id="8524c-105">Input Registers</span></span>



| <span data-ttu-id="8524c-106">Registrarse</span><span class="sxs-lookup"><span data-stu-id="8524c-106">Register</span></span>      | <span data-ttu-id="8524c-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="8524c-107">Name</span></span> | <span data-ttu-id="8524c-108">Count</span><span class="sxs-lookup"><span data-stu-id="8524c-108">Count</span></span>              | <span data-ttu-id="8524c-109">L/E</span><span class="sxs-lookup"><span data-stu-id="8524c-109">R/W</span></span> | <span data-ttu-id="8524c-110">Dimensión</span><span class="sxs-lookup"><span data-stu-id="8524c-110">Dimension</span></span> | <span data-ttu-id="8524c-111">Indexable por r\#</span><span class="sxs-lookup"><span data-stu-id="8524c-111">Indexable by r\#</span></span> | <span data-ttu-id="8524c-112">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="8524c-112">Defaults</span></span> | <span data-ttu-id="8524c-113">Requiere DCL</span><span class="sxs-lookup"><span data-stu-id="8524c-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="8524c-114">c\#</span><span class="sxs-lookup"><span data-stu-id="8524c-114">r\#</span></span>           |      | <span data-ttu-id="8524c-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="8524c-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="8524c-116">L/E</span><span class="sxs-lookup"><span data-stu-id="8524c-116">R/W</span></span> | <span data-ttu-id="8524c-117">4</span><span class="sxs-lookup"><span data-stu-id="8524c-117">4</span></span>         | <span data-ttu-id="8524c-118">No</span><span class="sxs-lookup"><span data-stu-id="8524c-118">No</span></span>               | <span data-ttu-id="8524c-119">None</span><span class="sxs-lookup"><span data-stu-id="8524c-119">None</span></span>     | <span data-ttu-id="8524c-120">Sí</span><span class="sxs-lookup"><span data-stu-id="8524c-120">Yes</span></span>          |
| <span data-ttu-id="8524c-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="8524c-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="8524c-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="8524c-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="8524c-123">L/E</span><span class="sxs-lookup"><span data-stu-id="8524c-123">R/W</span></span> | <span data-ttu-id="8524c-124">4</span><span class="sxs-lookup"><span data-stu-id="8524c-124">4</span></span>         | <span data-ttu-id="8524c-125">Sí</span><span class="sxs-lookup"><span data-stu-id="8524c-125">Yes</span></span>              | <span data-ttu-id="8524c-126">None</span><span class="sxs-lookup"><span data-stu-id="8524c-126">None</span></span>     | <span data-ttu-id="8524c-127">Sí</span><span class="sxs-lookup"><span data-stu-id="8524c-127">Yes</span></span>          |
| <span data-ttu-id="8524c-128">v\#</span><span class="sxs-lookup"><span data-stu-id="8524c-128">v\#</span></span>           |      | <span data-ttu-id="8524c-129">32</span><span class="sxs-lookup"><span data-stu-id="8524c-129">32</span></span>                 | <span data-ttu-id="8524c-130">R</span><span class="sxs-lookup"><span data-stu-id="8524c-130">R</span></span>   | <span data-ttu-id="8524c-131">4</span><span class="sxs-lookup"><span data-stu-id="8524c-131">4</span></span>         | <span data-ttu-id="8524c-132">Sí</span><span class="sxs-lookup"><span data-stu-id="8524c-132">Yes</span></span>              | <span data-ttu-id="8524c-133">None</span><span class="sxs-lookup"><span data-stu-id="8524c-133">None</span></span>     | <span data-ttu-id="8524c-134">Sí</span><span class="sxs-lookup"><span data-stu-id="8524c-134">Yes</span></span>          |
| <span data-ttu-id="8524c-135">h\#</span><span class="sxs-lookup"><span data-stu-id="8524c-135">t\#</span></span>           |      | <span data-ttu-id="8524c-136">128</span><span class="sxs-lookup"><span data-stu-id="8524c-136">128</span></span>                | <span data-ttu-id="8524c-137">R</span><span class="sxs-lookup"><span data-stu-id="8524c-137">R</span></span>   | <span data-ttu-id="8524c-138">1</span><span class="sxs-lookup"><span data-stu-id="8524c-138">1</span></span>         | <span data-ttu-id="8524c-139">No</span><span class="sxs-lookup"><span data-stu-id="8524c-139">No</span></span>               | <span data-ttu-id="8524c-140">None</span><span class="sxs-lookup"><span data-stu-id="8524c-140">None</span></span>     | <span data-ttu-id="8524c-141">Sí</span><span class="sxs-lookup"><span data-stu-id="8524c-141">Yes</span></span>          |
| <span data-ttu-id="8524c-142">s\#</span><span class="sxs-lookup"><span data-stu-id="8524c-142">s\#</span></span>           |      | <span data-ttu-id="8524c-143">16</span><span class="sxs-lookup"><span data-stu-id="8524c-143">16</span></span>                 | <span data-ttu-id="8524c-144">R</span><span class="sxs-lookup"><span data-stu-id="8524c-144">R</span></span>   | <span data-ttu-id="8524c-145">1</span><span class="sxs-lookup"><span data-stu-id="8524c-145">1</span></span>         | <span data-ttu-id="8524c-146">No</span><span class="sxs-lookup"><span data-stu-id="8524c-146">No</span></span>               | <span data-ttu-id="8524c-147">None</span><span class="sxs-lookup"><span data-stu-id="8524c-147">None</span></span>     | <span data-ttu-id="8524c-148">Sí</span><span class="sxs-lookup"><span data-stu-id="8524c-148">Yes</span></span>          |
| <span data-ttu-id="8524c-149">\# \[ Índice CB\]</span><span class="sxs-lookup"><span data-stu-id="8524c-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="8524c-150">15</span><span class="sxs-lookup"><span data-stu-id="8524c-150">15</span></span>                 | <span data-ttu-id="8524c-151">R</span><span class="sxs-lookup"><span data-stu-id="8524c-151">R</span></span>   | <span data-ttu-id="8524c-152">4</span><span class="sxs-lookup"><span data-stu-id="8524c-152">4</span></span>         | <span data-ttu-id="8524c-153">Sí (contenido)</span><span class="sxs-lookup"><span data-stu-id="8524c-153">Yes(Contents)</span></span>    | <span data-ttu-id="8524c-154">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8524c-154">None</span></span>     | <span data-ttu-id="8524c-155">Sí</span><span class="sxs-lookup"><span data-stu-id="8524c-155">Yes</span></span>          |
| <span data-ttu-id="8524c-156">Índice de ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="8524c-156">icb\[index\]</span></span>  |      | <span data-ttu-id="8524c-157">1</span><span class="sxs-lookup"><span data-stu-id="8524c-157">1</span></span>                  | <span data-ttu-id="8524c-158">R</span><span class="sxs-lookup"><span data-stu-id="8524c-158">R</span></span>   | <span data-ttu-id="8524c-159">4</span><span class="sxs-lookup"><span data-stu-id="8524c-159">4</span></span>         | <span data-ttu-id="8524c-160">Sí (contenido)</span><span class="sxs-lookup"><span data-stu-id="8524c-160">Yes(Contents)</span></span>    | <span data-ttu-id="8524c-161">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8524c-161">None</span></span>     | <span data-ttu-id="8524c-162">Sí</span><span class="sxs-lookup"><span data-stu-id="8524c-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="8524c-163">Registros de salida</span><span class="sxs-lookup"><span data-stu-id="8524c-163">Output Registers</span></span>



| <span data-ttu-id="8524c-164">Registrarse</span><span class="sxs-lookup"><span data-stu-id="8524c-164">Register</span></span> | <span data-ttu-id="8524c-165">Nombre</span><span class="sxs-lookup"><span data-stu-id="8524c-165">Name</span></span>            | <span data-ttu-id="8524c-166">Count</span><span class="sxs-lookup"><span data-stu-id="8524c-166">Count</span></span> | <span data-ttu-id="8524c-167">L/E</span><span class="sxs-lookup"><span data-stu-id="8524c-167">R/W</span></span> | <span data-ttu-id="8524c-168">Dimensión</span><span class="sxs-lookup"><span data-stu-id="8524c-168">Dimension</span></span> | <span data-ttu-id="8524c-169">Indexable por r\#</span><span class="sxs-lookup"><span data-stu-id="8524c-169">Indexable by r\#</span></span> | <span data-ttu-id="8524c-170">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="8524c-170">Defaults</span></span> | <span data-ttu-id="8524c-171">Requiere DCL</span><span class="sxs-lookup"><span data-stu-id="8524c-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="8524c-172">NULL</span><span class="sxs-lookup"><span data-stu-id="8524c-172">NULL</span></span>     | <span data-ttu-id="8524c-173">Descartar resultado</span><span class="sxs-lookup"><span data-stu-id="8524c-173">Discard Result</span></span>  | <span data-ttu-id="8524c-174">N/D</span><span class="sxs-lookup"><span data-stu-id="8524c-174">N/A</span></span>   | <span data-ttu-id="8524c-175">W</span><span class="sxs-lookup"><span data-stu-id="8524c-175">W</span></span>   | <span data-ttu-id="8524c-176">N/D</span><span class="sxs-lookup"><span data-stu-id="8524c-176">N/A</span></span>       | <span data-ttu-id="8524c-177">N/D</span><span class="sxs-lookup"><span data-stu-id="8524c-177">N/A</span></span>              | <span data-ttu-id="8524c-178">N/D</span><span class="sxs-lookup"><span data-stu-id="8524c-178">N/A</span></span>      | <span data-ttu-id="8524c-179">No</span><span class="sxs-lookup"><span data-stu-id="8524c-179">No</span></span>           |
| <span data-ttu-id="8524c-180">aceptar\#</span><span class="sxs-lookup"><span data-stu-id="8524c-180">o\#</span></span>      | <span data-ttu-id="8524c-181">Registro de salida</span><span class="sxs-lookup"><span data-stu-id="8524c-181">Output Register</span></span> | <span data-ttu-id="8524c-182">8</span><span class="sxs-lookup"><span data-stu-id="8524c-182">8</span></span>     | <span data-ttu-id="8524c-183">W</span><span class="sxs-lookup"><span data-stu-id="8524c-183">W</span></span>   | <span data-ttu-id="8524c-184">N/D</span><span class="sxs-lookup"><span data-stu-id="8524c-184">N/A</span></span>       | <span data-ttu-id="8524c-185">N/D</span><span class="sxs-lookup"><span data-stu-id="8524c-185">N/A</span></span>              | <span data-ttu-id="8524c-186">4</span><span class="sxs-lookup"><span data-stu-id="8524c-186">4</span></span>        | <span data-ttu-id="8524c-187">No</span><span class="sxs-lookup"><span data-stu-id="8524c-187">No</span></span>           |
| <span data-ttu-id="8524c-188">oDepth</span><span class="sxs-lookup"><span data-stu-id="8524c-188">oDepth</span></span>   | <span data-ttu-id="8524c-189">Profundidad de salida</span><span class="sxs-lookup"><span data-stu-id="8524c-189">Output Depth</span></span>    | <span data-ttu-id="8524c-190">1</span><span class="sxs-lookup"><span data-stu-id="8524c-190">1</span></span>     | <span data-ttu-id="8524c-191">W</span><span class="sxs-lookup"><span data-stu-id="8524c-191">W</span></span>   | <span data-ttu-id="8524c-192">N/D</span><span class="sxs-lookup"><span data-stu-id="8524c-192">N/A</span></span>       | <span data-ttu-id="8524c-193">N/D</span><span class="sxs-lookup"><span data-stu-id="8524c-193">N/A</span></span>              | <span data-ttu-id="8524c-194">1</span><span class="sxs-lookup"><span data-stu-id="8524c-194">1</span></span>        | <span data-ttu-id="8524c-195">N/D</span><span class="sxs-lookup"><span data-stu-id="8524c-195">N/A</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="8524c-196">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8524c-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8524c-197">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8524c-197">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




