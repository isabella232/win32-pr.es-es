---
title: 'Registros: gs_4_1'
description: Esta sección contiene información de referencia de los registros de entrada y salida implementados por las versiones 4 \_ 0 y 4 1 del sombreador de geometría \_ .
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268961"
---
# <a name="registers---gs_4_1"></a><span data-ttu-id="11685-103">Registros: GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="11685-103">Registers - gs\_4\_1</span></span>

<span data-ttu-id="11685-104">Esta sección contiene información de referencia de los registros de entrada y salida implementados por las versiones 4 \_ 0 y 4 1 del sombreador de geometría \_ .</span><span class="sxs-lookup"><span data-stu-id="11685-104">This section contains reference information for the input and output registers implemented by geometry shader versions 4\_0 and 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="11685-105">Registros de entrada</span><span class="sxs-lookup"><span data-stu-id="11685-105">Input Registers</span></span>



| <span data-ttu-id="11685-106">Registrarse</span><span class="sxs-lookup"><span data-stu-id="11685-106">Register</span></span>                 | <span data-ttu-id="11685-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="11685-107">Name</span></span> | <span data-ttu-id="11685-108">Count</span><span class="sxs-lookup"><span data-stu-id="11685-108">Count</span></span>              | <span data-ttu-id="11685-109">L/E</span><span class="sxs-lookup"><span data-stu-id="11685-109">R/W</span></span> | <span data-ttu-id="11685-110">Dimensión</span><span class="sxs-lookup"><span data-stu-id="11685-110">Dimension</span></span>        | <span data-ttu-id="11685-111">Indexable por r\#</span><span class="sxs-lookup"><span data-stu-id="11685-111">Indexable by r\#</span></span> | <span data-ttu-id="11685-112">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="11685-112">Defaults</span></span> | <span data-ttu-id="11685-113">Requiere DCL</span><span class="sxs-lookup"><span data-stu-id="11685-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="11685-114">c\#</span><span class="sxs-lookup"><span data-stu-id="11685-114">r\#</span></span>                      |      | <span data-ttu-id="11685-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="11685-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="11685-116">L/E</span><span class="sxs-lookup"><span data-stu-id="11685-116">R/W</span></span> | <span data-ttu-id="11685-117">4</span><span class="sxs-lookup"><span data-stu-id="11685-117">4</span></span>                | <span data-ttu-id="11685-118">No</span><span class="sxs-lookup"><span data-stu-id="11685-118">No</span></span>               | <span data-ttu-id="11685-119">None</span><span class="sxs-lookup"><span data-stu-id="11685-119">None</span></span>     | <span data-ttu-id="11685-120">Sí</span><span class="sxs-lookup"><span data-stu-id="11685-120">Yes</span></span>          |
| <span data-ttu-id="11685-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="11685-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="11685-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="11685-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="11685-123">L/E</span><span class="sxs-lookup"><span data-stu-id="11685-123">R/W</span></span> | <span data-ttu-id="11685-124">4</span><span class="sxs-lookup"><span data-stu-id="11685-124">4</span></span>                | <span data-ttu-id="11685-125">Sí</span><span class="sxs-lookup"><span data-stu-id="11685-125">Yes</span></span>              | <span data-ttu-id="11685-126">None</span><span class="sxs-lookup"><span data-stu-id="11685-126">None</span></span>     | <span data-ttu-id="11685-127">Sí</span><span class="sxs-lookup"><span data-stu-id="11685-127">Yes</span></span>          |
| <span data-ttu-id="11685-128">\# \[ elemento de vértice \] \[ v\]</span><span class="sxs-lookup"><span data-stu-id="11685-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="11685-129">32</span><span class="sxs-lookup"><span data-stu-id="11685-129">32</span></span>                 | <span data-ttu-id="11685-130">R</span><span class="sxs-lookup"><span data-stu-id="11685-130">R</span></span>   | <span data-ttu-id="11685-131">4 (COMP) \* 6 (Vert)</span><span class="sxs-lookup"><span data-stu-id="11685-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="11685-132">Sí</span><span class="sxs-lookup"><span data-stu-id="11685-132">Yes</span></span>              | <span data-ttu-id="11685-133">None</span><span class="sxs-lookup"><span data-stu-id="11685-133">None</span></span>     | <span data-ttu-id="11685-134">Sí</span><span class="sxs-lookup"><span data-stu-id="11685-134">Yes</span></span>          |
| <span data-ttu-id="11685-135">vprim</span><span class="sxs-lookup"><span data-stu-id="11685-135">vprim</span></span>                    |      | <span data-ttu-id="11685-136">1</span><span class="sxs-lookup"><span data-stu-id="11685-136">1</span></span>                  | <span data-ttu-id="11685-137">R</span><span class="sxs-lookup"><span data-stu-id="11685-137">R</span></span>   | <span data-ttu-id="11685-138">1</span><span class="sxs-lookup"><span data-stu-id="11685-138">1</span></span>                | <span data-ttu-id="11685-139">No</span><span class="sxs-lookup"><span data-stu-id="11685-139">No</span></span>               | <span data-ttu-id="11685-140">None</span><span class="sxs-lookup"><span data-stu-id="11685-140">None</span></span>     | <span data-ttu-id="11685-141">Sí</span><span class="sxs-lookup"><span data-stu-id="11685-141">Yes</span></span>          |
| <span data-ttu-id="11685-142">h\#</span><span class="sxs-lookup"><span data-stu-id="11685-142">t\#</span></span>                      |      | <span data-ttu-id="11685-143">128</span><span class="sxs-lookup"><span data-stu-id="11685-143">128</span></span>                | <span data-ttu-id="11685-144">R</span><span class="sxs-lookup"><span data-stu-id="11685-144">R</span></span>   | <span data-ttu-id="11685-145">1</span><span class="sxs-lookup"><span data-stu-id="11685-145">1</span></span>                | <span data-ttu-id="11685-146">No</span><span class="sxs-lookup"><span data-stu-id="11685-146">No</span></span>               | <span data-ttu-id="11685-147">None</span><span class="sxs-lookup"><span data-stu-id="11685-147">None</span></span>     | <span data-ttu-id="11685-148">Sí</span><span class="sxs-lookup"><span data-stu-id="11685-148">Yes</span></span>          |
| <span data-ttu-id="11685-149">s\#</span><span class="sxs-lookup"><span data-stu-id="11685-149">s\#</span></span>                      |      | <span data-ttu-id="11685-150">16</span><span class="sxs-lookup"><span data-stu-id="11685-150">16</span></span>                 | <span data-ttu-id="11685-151">R</span><span class="sxs-lookup"><span data-stu-id="11685-151">R</span></span>   | <span data-ttu-id="11685-152">1</span><span class="sxs-lookup"><span data-stu-id="11685-152">1</span></span>                | <span data-ttu-id="11685-153">No</span><span class="sxs-lookup"><span data-stu-id="11685-153">No</span></span>               | <span data-ttu-id="11685-154">None</span><span class="sxs-lookup"><span data-stu-id="11685-154">None</span></span>     | <span data-ttu-id="11685-155">Sí</span><span class="sxs-lookup"><span data-stu-id="11685-155">Yes</span></span>          |
| <span data-ttu-id="11685-156">\# \[ Índice CB\]</span><span class="sxs-lookup"><span data-stu-id="11685-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="11685-157">15</span><span class="sxs-lookup"><span data-stu-id="11685-157">15</span></span>                 | <span data-ttu-id="11685-158">R</span><span class="sxs-lookup"><span data-stu-id="11685-158">R</span></span>   | <span data-ttu-id="11685-159">4</span><span class="sxs-lookup"><span data-stu-id="11685-159">4</span></span>                | <span data-ttu-id="11685-160">Sí (contenido)</span><span class="sxs-lookup"><span data-stu-id="11685-160">Yes(Contents)</span></span>    | <span data-ttu-id="11685-161">Ninguno</span><span class="sxs-lookup"><span data-stu-id="11685-161">None</span></span>     | <span data-ttu-id="11685-162">Sí</span><span class="sxs-lookup"><span data-stu-id="11685-162">Yes</span></span>          |
| <span data-ttu-id="11685-163">Índice de ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="11685-163">icb\[index\]</span></span>             |      | <span data-ttu-id="11685-164">1</span><span class="sxs-lookup"><span data-stu-id="11685-164">1</span></span>                  | <span data-ttu-id="11685-165">R</span><span class="sxs-lookup"><span data-stu-id="11685-165">R</span></span>   | <span data-ttu-id="11685-166">4</span><span class="sxs-lookup"><span data-stu-id="11685-166">4</span></span>                | <span data-ttu-id="11685-167">Sí (contenido)</span><span class="sxs-lookup"><span data-stu-id="11685-167">Yes(Contents)</span></span>    | <span data-ttu-id="11685-168">Ninguno</span><span class="sxs-lookup"><span data-stu-id="11685-168">None</span></span>     | <span data-ttu-id="11685-169">Sí</span><span class="sxs-lookup"><span data-stu-id="11685-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="11685-170">Registros de salida</span><span class="sxs-lookup"><span data-stu-id="11685-170">Output Registers</span></span>



| <span data-ttu-id="11685-171">Registrarse</span><span class="sxs-lookup"><span data-stu-id="11685-171">Register</span></span> | <span data-ttu-id="11685-172">Nombre</span><span class="sxs-lookup"><span data-stu-id="11685-172">Name</span></span>            | <span data-ttu-id="11685-173">Count</span><span class="sxs-lookup"><span data-stu-id="11685-173">Count</span></span> | <span data-ttu-id="11685-174">L/E</span><span class="sxs-lookup"><span data-stu-id="11685-174">R/W</span></span> | <span data-ttu-id="11685-175">Dimensión</span><span class="sxs-lookup"><span data-stu-id="11685-175">Dimension</span></span> | <span data-ttu-id="11685-176">Indexable por r\#</span><span class="sxs-lookup"><span data-stu-id="11685-176">Indexable by r\#</span></span> | <span data-ttu-id="11685-177">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="11685-177">Defaults</span></span> | <span data-ttu-id="11685-178">Requiere DCL</span><span class="sxs-lookup"><span data-stu-id="11685-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="11685-179">NULL</span><span class="sxs-lookup"><span data-stu-id="11685-179">NULL</span></span>     | <span data-ttu-id="11685-180">Descartar resultado</span><span class="sxs-lookup"><span data-stu-id="11685-180">Discard Result</span></span>  | <span data-ttu-id="11685-181">N/D</span><span class="sxs-lookup"><span data-stu-id="11685-181">N/A</span></span>   | <span data-ttu-id="11685-182">W</span><span class="sxs-lookup"><span data-stu-id="11685-182">W</span></span>   | <span data-ttu-id="11685-183">N/D</span><span class="sxs-lookup"><span data-stu-id="11685-183">N/A</span></span>       | <span data-ttu-id="11685-184">N/D</span><span class="sxs-lookup"><span data-stu-id="11685-184">N/A</span></span>              | <span data-ttu-id="11685-185">N/D</span><span class="sxs-lookup"><span data-stu-id="11685-185">N/A</span></span>      | <span data-ttu-id="11685-186">No</span><span class="sxs-lookup"><span data-stu-id="11685-186">No</span></span>           |
| <span data-ttu-id="11685-187">aceptar\#</span><span class="sxs-lookup"><span data-stu-id="11685-187">o\#</span></span>      | <span data-ttu-id="11685-188">Registro de salida</span><span class="sxs-lookup"><span data-stu-id="11685-188">Output Register</span></span> | <span data-ttu-id="11685-189">32</span><span class="sxs-lookup"><span data-stu-id="11685-189">32</span></span>    | <span data-ttu-id="11685-190">W</span><span class="sxs-lookup"><span data-stu-id="11685-190">W</span></span>   | <span data-ttu-id="11685-191">N/D</span><span class="sxs-lookup"><span data-stu-id="11685-191">N/A</span></span>       | <span data-ttu-id="11685-192">N/D</span><span class="sxs-lookup"><span data-stu-id="11685-192">N/A</span></span>              | <span data-ttu-id="11685-193">4</span><span class="sxs-lookup"><span data-stu-id="11685-193">4</span></span>        | <span data-ttu-id="11685-194">Sí</span><span class="sxs-lookup"><span data-stu-id="11685-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="11685-195">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11685-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11685-196">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="11685-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




