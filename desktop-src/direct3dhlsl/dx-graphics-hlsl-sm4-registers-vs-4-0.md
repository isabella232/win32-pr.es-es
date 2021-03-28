---
title: 'Registros: vs_4_0'
description: Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de vértices versión 4 \_ 0.
ms.assetid: f471df6a-06f6-4783-ba8f-cf0a3b43727f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 425fc4174b1c4a103fc7db15b5f05ae2b6dd95e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996760"
---
# <a name="registers---vs_4_0"></a><span data-ttu-id="942af-103">Registros-vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="942af-103">Registers - vs\_4\_0</span></span>

<span data-ttu-id="942af-104">Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de vértices versión 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="942af-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="942af-105">Registros de entrada</span><span class="sxs-lookup"><span data-stu-id="942af-105">Input Registers</span></span>



| <span data-ttu-id="942af-106">Registrarse</span><span class="sxs-lookup"><span data-stu-id="942af-106">Register</span></span>      | <span data-ttu-id="942af-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="942af-107">Name</span></span> | <span data-ttu-id="942af-108">Count</span><span class="sxs-lookup"><span data-stu-id="942af-108">Count</span></span>              | <span data-ttu-id="942af-109">L/E</span><span class="sxs-lookup"><span data-stu-id="942af-109">R/W</span></span> | <span data-ttu-id="942af-110">Dimensión</span><span class="sxs-lookup"><span data-stu-id="942af-110">Dimension</span></span> | <span data-ttu-id="942af-111">Indexable por r\#</span><span class="sxs-lookup"><span data-stu-id="942af-111">Indexable by r\#</span></span> | <span data-ttu-id="942af-112">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="942af-112">Defaults</span></span> | <span data-ttu-id="942af-113">Requiere DCL</span><span class="sxs-lookup"><span data-stu-id="942af-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="942af-114">c\#</span><span class="sxs-lookup"><span data-stu-id="942af-114">r\#</span></span>           |      | <span data-ttu-id="942af-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="942af-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="942af-116">L/E</span><span class="sxs-lookup"><span data-stu-id="942af-116">R/W</span></span> | <span data-ttu-id="942af-117">4</span><span class="sxs-lookup"><span data-stu-id="942af-117">4</span></span>         | <span data-ttu-id="942af-118">No</span><span class="sxs-lookup"><span data-stu-id="942af-118">No</span></span>               | <span data-ttu-id="942af-119">None</span><span class="sxs-lookup"><span data-stu-id="942af-119">None</span></span>     | <span data-ttu-id="942af-120">Sí</span><span class="sxs-lookup"><span data-stu-id="942af-120">Yes</span></span>          |
| <span data-ttu-id="942af-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="942af-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="942af-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="942af-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="942af-123">L/E</span><span class="sxs-lookup"><span data-stu-id="942af-123">R/W</span></span> | <span data-ttu-id="942af-124">4</span><span class="sxs-lookup"><span data-stu-id="942af-124">4</span></span>         | <span data-ttu-id="942af-125">Sí</span><span class="sxs-lookup"><span data-stu-id="942af-125">Yes</span></span>              | <span data-ttu-id="942af-126">None</span><span class="sxs-lookup"><span data-stu-id="942af-126">None</span></span>     | <span data-ttu-id="942af-127">Sí</span><span class="sxs-lookup"><span data-stu-id="942af-127">Yes</span></span>          |
| <span data-ttu-id="942af-128">v\#</span><span class="sxs-lookup"><span data-stu-id="942af-128">v\#</span></span>           |      | <span data-ttu-id="942af-129">16</span><span class="sxs-lookup"><span data-stu-id="942af-129">16</span></span>                 | <span data-ttu-id="942af-130">R</span><span class="sxs-lookup"><span data-stu-id="942af-130">R</span></span>   | <span data-ttu-id="942af-131">4</span><span class="sxs-lookup"><span data-stu-id="942af-131">4</span></span>         | <span data-ttu-id="942af-132">Sí</span><span class="sxs-lookup"><span data-stu-id="942af-132">Yes</span></span>              | <span data-ttu-id="942af-133">None</span><span class="sxs-lookup"><span data-stu-id="942af-133">None</span></span>     | <span data-ttu-id="942af-134">Sí</span><span class="sxs-lookup"><span data-stu-id="942af-134">Yes</span></span>          |
| <span data-ttu-id="942af-135">h\#</span><span class="sxs-lookup"><span data-stu-id="942af-135">t\#</span></span>           |      | <span data-ttu-id="942af-136">128</span><span class="sxs-lookup"><span data-stu-id="942af-136">128</span></span>                | <span data-ttu-id="942af-137">R</span><span class="sxs-lookup"><span data-stu-id="942af-137">R</span></span>   | <span data-ttu-id="942af-138">1</span><span class="sxs-lookup"><span data-stu-id="942af-138">1</span></span>         | <span data-ttu-id="942af-139">No</span><span class="sxs-lookup"><span data-stu-id="942af-139">No</span></span>               | <span data-ttu-id="942af-140">None</span><span class="sxs-lookup"><span data-stu-id="942af-140">None</span></span>     | <span data-ttu-id="942af-141">Sí</span><span class="sxs-lookup"><span data-stu-id="942af-141">Yes</span></span>          |
| <span data-ttu-id="942af-142">s\#</span><span class="sxs-lookup"><span data-stu-id="942af-142">s\#</span></span>           |      | <span data-ttu-id="942af-143">16</span><span class="sxs-lookup"><span data-stu-id="942af-143">16</span></span>                 | <span data-ttu-id="942af-144">R</span><span class="sxs-lookup"><span data-stu-id="942af-144">R</span></span>   | <span data-ttu-id="942af-145">1</span><span class="sxs-lookup"><span data-stu-id="942af-145">1</span></span>         | <span data-ttu-id="942af-146">No</span><span class="sxs-lookup"><span data-stu-id="942af-146">No</span></span>               | <span data-ttu-id="942af-147">None</span><span class="sxs-lookup"><span data-stu-id="942af-147">None</span></span>     | <span data-ttu-id="942af-148">Sí</span><span class="sxs-lookup"><span data-stu-id="942af-148">Yes</span></span>          |
| <span data-ttu-id="942af-149">\# \[ Índice CB\]</span><span class="sxs-lookup"><span data-stu-id="942af-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="942af-150">15</span><span class="sxs-lookup"><span data-stu-id="942af-150">15</span></span>                 | <span data-ttu-id="942af-151">R</span><span class="sxs-lookup"><span data-stu-id="942af-151">R</span></span>   | <span data-ttu-id="942af-152">4</span><span class="sxs-lookup"><span data-stu-id="942af-152">4</span></span>         | <span data-ttu-id="942af-153">Sí (contenido)</span><span class="sxs-lookup"><span data-stu-id="942af-153">Yes(Contents)</span></span>    | <span data-ttu-id="942af-154">Ninguno</span><span class="sxs-lookup"><span data-stu-id="942af-154">None</span></span>     | <span data-ttu-id="942af-155">Sí</span><span class="sxs-lookup"><span data-stu-id="942af-155">Yes</span></span>          |
| <span data-ttu-id="942af-156">Índice de ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="942af-156">icb\[index\]</span></span>  |      | <span data-ttu-id="942af-157">1</span><span class="sxs-lookup"><span data-stu-id="942af-157">1</span></span>                  | <span data-ttu-id="942af-158">R</span><span class="sxs-lookup"><span data-stu-id="942af-158">R</span></span>   | <span data-ttu-id="942af-159">4</span><span class="sxs-lookup"><span data-stu-id="942af-159">4</span></span>         | <span data-ttu-id="942af-160">Sí (contenido)</span><span class="sxs-lookup"><span data-stu-id="942af-160">Yes(Contents)</span></span>    | <span data-ttu-id="942af-161">Ninguno</span><span class="sxs-lookup"><span data-stu-id="942af-161">None</span></span>     | <span data-ttu-id="942af-162">Sí</span><span class="sxs-lookup"><span data-stu-id="942af-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="942af-163">Registros de salida</span><span class="sxs-lookup"><span data-stu-id="942af-163">Output Registers</span></span>



| <span data-ttu-id="942af-164">Registrarse</span><span class="sxs-lookup"><span data-stu-id="942af-164">Register</span></span> | <span data-ttu-id="942af-165">Nombre</span><span class="sxs-lookup"><span data-stu-id="942af-165">Name</span></span>            | <span data-ttu-id="942af-166">Count</span><span class="sxs-lookup"><span data-stu-id="942af-166">Count</span></span> | <span data-ttu-id="942af-167">L/E</span><span class="sxs-lookup"><span data-stu-id="942af-167">R/W</span></span> | <span data-ttu-id="942af-168">Dimensión</span><span class="sxs-lookup"><span data-stu-id="942af-168">Dimension</span></span> | <span data-ttu-id="942af-169">Indexable por r\#</span><span class="sxs-lookup"><span data-stu-id="942af-169">Indexable by r\#</span></span> | <span data-ttu-id="942af-170">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="942af-170">Defaults</span></span> | <span data-ttu-id="942af-171">Requiere DCL</span><span class="sxs-lookup"><span data-stu-id="942af-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="942af-172">NULL</span><span class="sxs-lookup"><span data-stu-id="942af-172">NULL</span></span>     | <span data-ttu-id="942af-173">Descartar resultado</span><span class="sxs-lookup"><span data-stu-id="942af-173">Discard Result</span></span>  | <span data-ttu-id="942af-174">N/D</span><span class="sxs-lookup"><span data-stu-id="942af-174">N/A</span></span>   | <span data-ttu-id="942af-175">W</span><span class="sxs-lookup"><span data-stu-id="942af-175">W</span></span>   | <span data-ttu-id="942af-176">N/D</span><span class="sxs-lookup"><span data-stu-id="942af-176">N/A</span></span>       | <span data-ttu-id="942af-177">N/D</span><span class="sxs-lookup"><span data-stu-id="942af-177">N/A</span></span>              | <span data-ttu-id="942af-178">N/D</span><span class="sxs-lookup"><span data-stu-id="942af-178">N/A</span></span>      | <span data-ttu-id="942af-179">No</span><span class="sxs-lookup"><span data-stu-id="942af-179">No</span></span>           |
| <span data-ttu-id="942af-180">aceptar\#</span><span class="sxs-lookup"><span data-stu-id="942af-180">o\#</span></span>      | <span data-ttu-id="942af-181">Registro de salida</span><span class="sxs-lookup"><span data-stu-id="942af-181">Output Register</span></span> | <span data-ttu-id="942af-182">16</span><span class="sxs-lookup"><span data-stu-id="942af-182">16</span></span>    | <span data-ttu-id="942af-183">W</span><span class="sxs-lookup"><span data-stu-id="942af-183">W</span></span>   | <span data-ttu-id="942af-184">N/D</span><span class="sxs-lookup"><span data-stu-id="942af-184">N/A</span></span>       | <span data-ttu-id="942af-185">N/D</span><span class="sxs-lookup"><span data-stu-id="942af-185">N/A</span></span>              | <span data-ttu-id="942af-186">4</span><span class="sxs-lookup"><span data-stu-id="942af-186">4</span></span>        | <span data-ttu-id="942af-187">Sí</span><span class="sxs-lookup"><span data-stu-id="942af-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="942af-188">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="942af-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="942af-189">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="942af-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




