---
title: dcl_resource estructurado (SM5-ASM)
description: Declare una entrada de recurso de sombreador y asígnela a un registro de marcador de posición t \-a para el recurso. | dcl_resource estructurado (SM5-ASM)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279987"
---
# <a name="dcl_resource-structured-sm5---asm"></a><span data-ttu-id="e8fc0-104">\_recurso de DCL estructurado (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e8fc0-104">dcl\_resource structured (sm5 - asm)</span></span>

<span data-ttu-id="e8fc0-105">Declare una entrada de recurso de sombreador y asígnela a un \# registro de marcador de posición t-a para el recurso.</span><span class="sxs-lookup"><span data-stu-id="e8fc0-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="e8fc0-106">\_recurso \_ de DCL estructurado DstSRV, structByteStride</span><span class="sxs-lookup"><span data-stu-id="e8fc0-106">dcl\_resource\_structured dstSRV, structByteStride</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="e8fc0-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="e8fc0-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="e8fc0-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8fc0-108">Description</span></span>                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fc0-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span><span class="sxs-lookup"><span data-stu-id="e8fc0-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/>                                         | <span data-ttu-id="e8fc0-110">\[en \] un \# registro t declarado como una referencia a un ShaderResourceView de un búfer estructurado con el intervalo especificado que se debe enlazar a la ranura SRV \# en la API.</span><span class="sxs-lookup"><span data-stu-id="e8fc0-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a structured buffer with the specified stride that must be bound to SRV slot \# at the API.</span></span> <br/> |
| <span data-ttu-id="e8fc0-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="e8fc0-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="e8fc0-112">\[en \] un uint que especifica el tamaño de la estructura en bytes del búfer que se está declarando.</span><span class="sxs-lookup"><span data-stu-id="e8fc0-112">\[in\] A uint that specifies the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="e8fc0-113">Este valor debe ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="e8fc0-113">This value must be greater than zero.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="e8fc0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8fc0-114">Remarks</span></span>

<span data-ttu-id="e8fc0-115">El contenido de la estructura no tiene ningún tipo; las operaciones realizadas en la memoria pueden interpretar implícitamente los datos como si tuvieran un tipo.</span><span class="sxs-lookup"><span data-stu-id="e8fc0-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="e8fc0-116">Las instrucciones que hacen referencia a un t estructurado \# toman una dirección 2D, donde el primer componente selecciona \[ struct \] , y el segundo componente elige \[ offset en struct, múltiplo de 32 bits \] .</span><span class="sxs-lookup"><span data-stu-id="e8fc0-116">Instructions that reference a structured t\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, multiple of 32-bits\].</span></span>

<span data-ttu-id="e8fc0-117">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="e8fc0-117">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="e8fc0-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="e8fc0-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e8fc0-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="e8fc0-119">Vertex</span></span> | <span data-ttu-id="e8fc0-120">Casco</span><span class="sxs-lookup"><span data-stu-id="e8fc0-120">Hull</span></span> | <span data-ttu-id="e8fc0-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="e8fc0-121">Domain</span></span> | <span data-ttu-id="e8fc0-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="e8fc0-122">Geometry</span></span> | <span data-ttu-id="e8fc0-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="e8fc0-123">Pixel</span></span> | <span data-ttu-id="e8fc0-124">Compute</span><span class="sxs-lookup"><span data-stu-id="e8fc0-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e8fc0-125">X</span><span class="sxs-lookup"><span data-stu-id="e8fc0-125">X</span></span>      | <span data-ttu-id="e8fc0-126">X</span><span class="sxs-lookup"><span data-stu-id="e8fc0-126">X</span></span>    | <span data-ttu-id="e8fc0-127">X</span><span class="sxs-lookup"><span data-stu-id="e8fc0-127">X</span></span>      | <span data-ttu-id="e8fc0-128">X</span><span class="sxs-lookup"><span data-stu-id="e8fc0-128">X</span></span>        | <span data-ttu-id="e8fc0-129">X</span><span class="sxs-lookup"><span data-stu-id="e8fc0-129">X</span></span>     | <span data-ttu-id="e8fc0-130">X</span><span class="sxs-lookup"><span data-stu-id="e8fc0-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e8fc0-131">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e8fc0-131">Minimum Shader Model</span></span>

<span data-ttu-id="e8fc0-132">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e8fc0-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e8fc0-133">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e8fc0-133">Shader Model</span></span>                                              | <span data-ttu-id="e8fc0-134">Compatible</span><span class="sxs-lookup"><span data-stu-id="e8fc0-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e8fc0-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e8fc0-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e8fc0-136">sí</span><span class="sxs-lookup"><span data-stu-id="e8fc0-136">yes</span></span>       |
| [<span data-ttu-id="e8fc0-137">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e8fc0-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e8fc0-138">no</span><span class="sxs-lookup"><span data-stu-id="e8fc0-138">no</span></span>        |
| [<span data-ttu-id="e8fc0-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e8fc0-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e8fc0-140">no</span><span class="sxs-lookup"><span data-stu-id="e8fc0-140">no</span></span>        |
| [<span data-ttu-id="e8fc0-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8fc0-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e8fc0-142">no</span><span class="sxs-lookup"><span data-stu-id="e8fc0-142">no</span></span>        |
| [<span data-ttu-id="e8fc0-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8fc0-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e8fc0-144">no</span><span class="sxs-lookup"><span data-stu-id="e8fc0-144">no</span></span>        |
| [<span data-ttu-id="e8fc0-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8fc0-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e8fc0-146">no</span><span class="sxs-lookup"><span data-stu-id="e8fc0-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e8fc0-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8fc0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8fc0-148">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8fc0-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





