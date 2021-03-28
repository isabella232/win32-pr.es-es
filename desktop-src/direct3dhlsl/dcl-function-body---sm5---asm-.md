---
title: dcl_function_body (SM5-ASM)
description: Declarar un cuerpo de función.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104149009"
---
# <a name="dcl_function_body-sm5---asm"></a><span data-ttu-id="7e711-103">\_ \_ cuerpo de la función DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7e711-103">dcl\_function\_body (sm5 - asm)</span></span>

<span data-ttu-id="7e711-104">Declarar un cuerpo de función.</span><span class="sxs-lookup"><span data-stu-id="7e711-104">Declare a function body.</span></span>



| <span data-ttu-id="7e711-105">cuerpo de la función de DCL \_ \_ FB\#</span><span class="sxs-lookup"><span data-stu-id="7e711-105">dcl\_function\_body fb\#</span></span> |
|--------------------------|



 



| <span data-ttu-id="7e711-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e711-106">Item</span></span>                                                          | <span data-ttu-id="7e711-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e711-107">Description</span></span>                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="7e711-108"><span id="fb_"></span><span id="FB_"></span>*FB\#*</span><span class="sxs-lookup"><span data-stu-id="7e711-108"><span id="fb_"></span><span id="FB_"></span>*fb\#*</span></span><br/> | <span data-ttu-id="7e711-109">\[en \] la etiqueta del lugar donde aparecerá la función.</span><span class="sxs-lookup"><span data-stu-id="7e711-109">\[in\] The label of the place where the function will appear.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7e711-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e711-110">Remarks</span></span>

<span data-ttu-id="7e711-111">Esta instrucción declara un cuerpo de función único cuyo código aparecerá más adelante en el programa en la etiqueta FB \# .</span><span class="sxs-lookup"><span data-stu-id="7e711-111">This instruction declares a unique function body whose code will appear later in the program at label fb\#.</span></span>

<span data-ttu-id="7e711-112">Los cuerpos de función se utilizan en las declaraciones de tabla de función.</span><span class="sxs-lookup"><span data-stu-id="7e711-112">Function bodies are used in function table declarations.</span></span> <span data-ttu-id="7e711-113">Para obtener más información, consulte la [ \_ \_ tabla de funciones DCL](dcl-function-table---sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="7e711-113">For more info, see [dcl\_function\_table](dcl-function-table---sm5---asm-.md).</span></span>

<span data-ttu-id="7e711-114">En el sombreador de casco y el sombreador de dominios, donde hay varias fases (fase de punto de control, fase de bifurcación y fase de combinación), todos los cuerpos de función (etiqueta FB \# ) aparecen después de todas las fases, en lugar de agruparse por fase.</span><span class="sxs-lookup"><span data-stu-id="7e711-114">In the hull shader and domain shader, where there are multiple phases (control point phase, fork phase, and join phase), all function bodies (label fb\#) appear after all the phases, rather than being grouped by phase.</span></span>

<span data-ttu-id="7e711-115">No hay ningún límite en el número de cuerpos de función que pueden estar presentes.</span><span class="sxs-lookup"><span data-stu-id="7e711-115">There is no limit to how many function bodies can be present.</span></span>

<span data-ttu-id="7e711-116">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="7e711-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7e711-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="7e711-117">Vertex</span></span> | <span data-ttu-id="7e711-118">Casco</span><span class="sxs-lookup"><span data-stu-id="7e711-118">Hull</span></span> | <span data-ttu-id="7e711-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="7e711-119">Domain</span></span> | <span data-ttu-id="7e711-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="7e711-120">Geometry</span></span> | <span data-ttu-id="7e711-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="7e711-121">Pixel</span></span> | <span data-ttu-id="7e711-122">Compute</span><span class="sxs-lookup"><span data-stu-id="7e711-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7e711-123">X</span><span class="sxs-lookup"><span data-stu-id="7e711-123">X</span></span>      | <span data-ttu-id="7e711-124">X</span><span class="sxs-lookup"><span data-stu-id="7e711-124">X</span></span>    | <span data-ttu-id="7e711-125">X</span><span class="sxs-lookup"><span data-stu-id="7e711-125">X</span></span>      | <span data-ttu-id="7e711-126">X</span><span class="sxs-lookup"><span data-stu-id="7e711-126">X</span></span>        | <span data-ttu-id="7e711-127">X</span><span class="sxs-lookup"><span data-stu-id="7e711-127">X</span></span>     | <span data-ttu-id="7e711-128">X</span><span class="sxs-lookup"><span data-stu-id="7e711-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7e711-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="7e711-129">Minimum Shader Model</span></span>

<span data-ttu-id="7e711-130">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="7e711-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7e711-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7e711-131">Shader Model</span></span>                                              | <span data-ttu-id="7e711-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="7e711-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7e711-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7e711-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7e711-134">sí</span><span class="sxs-lookup"><span data-stu-id="7e711-134">yes</span></span>       |
| [<span data-ttu-id="7e711-135">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="7e711-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7e711-136">no</span><span class="sxs-lookup"><span data-stu-id="7e711-136">no</span></span>        |
| [<span data-ttu-id="7e711-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="7e711-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7e711-138">no</span><span class="sxs-lookup"><span data-stu-id="7e711-138">no</span></span>        |
| [<span data-ttu-id="7e711-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e711-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7e711-140">no</span><span class="sxs-lookup"><span data-stu-id="7e711-140">no</span></span>        |
| [<span data-ttu-id="7e711-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e711-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7e711-142">no</span><span class="sxs-lookup"><span data-stu-id="7e711-142">no</span></span>        |
| [<span data-ttu-id="7e711-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e711-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7e711-144">no</span><span class="sxs-lookup"><span data-stu-id="7e711-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7e711-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e711-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e711-146">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e711-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





