---
title: DFMA (SM5-ASM)
description: Realiza una adición con fusibles-Multiply.
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e6cafc71dbc7d57655524b1b87c9c5b9ba20f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358479"
---
# <a name="dfma-sm5---asm"></a><span data-ttu-id="9fdc5-103">DFMA (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9fdc5-103">dfma (sm5 - asm)</span></span>

<span data-ttu-id="9fdc5-104">Realiza una adición con fusibles-Multiply.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-104">Performs a fused-multiply add.</span></span>



| <span data-ttu-id="9fdc5-105">DFMA \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9fdc5-105">dfma\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],\[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9fdc5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="9fdc5-106">Item</span></span>                                                            | <span data-ttu-id="9fdc5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fdc5-107">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fdc5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9fdc5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9fdc5-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-109">\[in\] The address of the result of the operation.</span></span> <span data-ttu-id="9fdc5-110">El valor del resultado debe ser preciso para 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-110">The result value must be accurate to 0.5 ULP.</span></span><br/> <span data-ttu-id="9fdc5-111">*dest*  =  *src0* \* *SRC1*  +  *src2*</span><span class="sxs-lookup"><span data-stu-id="9fdc5-111">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="9fdc5-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9fdc5-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9fdc5-113">\[en \] los componentes que se van a multiplicar por *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-113">\[in\] The components to multiply with *src1*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="9fdc5-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="9fdc5-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="9fdc5-115">\[en \] los componentes que se van a multiplicar por *src0*.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-115">\[in\] The components to multiply with *src0*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="9fdc5-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="9fdc5-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="9fdc5-117">\[en \] los componentes que se van a agregar a *src0* \* *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-117">\[in\] The components to add to *src0* \* *src1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="9fdc5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fdc5-118">Remarks</span></span>

<span data-ttu-id="9fdc5-119">Los sombreadores que usan esta instrucción se marcarán con una marca de sombreador que hará que no se puedan enlazar a menos que se cumplan todas las condiciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-119">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="9fdc5-120">El sistema admite DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-120">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="9fdc5-121">El sistema incluye un controlador WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-121">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="9fdc5-122">El controlador informa de la compatibilidad con esta instrucción a través de **\_ las opciones de D3D11 de datos de características de D3D11 \_ \_ \_ . ExtendedDoublesShaderInstructions** establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="9fdc5-122">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="9fdc5-123">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="9fdc5-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9fdc5-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="9fdc5-124">Vertex</span></span> | <span data-ttu-id="9fdc5-125">Casco</span><span class="sxs-lookup"><span data-stu-id="9fdc5-125">Hull</span></span> | <span data-ttu-id="9fdc5-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="9fdc5-126">Domain</span></span> | <span data-ttu-id="9fdc5-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="9fdc5-127">Geometry</span></span> | <span data-ttu-id="9fdc5-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="9fdc5-128">Pixel</span></span> | <span data-ttu-id="9fdc5-129">Compute</span><span class="sxs-lookup"><span data-stu-id="9fdc5-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9fdc5-130">X</span><span class="sxs-lookup"><span data-stu-id="9fdc5-130">X</span></span>      | <span data-ttu-id="9fdc5-131">X</span><span class="sxs-lookup"><span data-stu-id="9fdc5-131">X</span></span>    | <span data-ttu-id="9fdc5-132">X</span><span class="sxs-lookup"><span data-stu-id="9fdc5-132">X</span></span>      | <span data-ttu-id="9fdc5-133">X</span><span class="sxs-lookup"><span data-stu-id="9fdc5-133">X</span></span>        | <span data-ttu-id="9fdc5-134">X</span><span class="sxs-lookup"><span data-stu-id="9fdc5-134">X</span></span>     | <span data-ttu-id="9fdc5-135">X</span><span class="sxs-lookup"><span data-stu-id="9fdc5-135">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9fdc5-136">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="9fdc5-136">Minimum Shader Model</span></span>

<span data-ttu-id="9fdc5-137">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9fdc5-137">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9fdc5-138">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="9fdc5-138">Shader Model</span></span>                                              | <span data-ttu-id="9fdc5-139">Compatible</span><span class="sxs-lookup"><span data-stu-id="9fdc5-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9fdc5-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9fdc5-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9fdc5-141">sí</span><span class="sxs-lookup"><span data-stu-id="9fdc5-141">yes</span></span>       |
| [<span data-ttu-id="9fdc5-142">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="9fdc5-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9fdc5-143">no</span><span class="sxs-lookup"><span data-stu-id="9fdc5-143">no</span></span>        |
| [<span data-ttu-id="9fdc5-144">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9fdc5-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9fdc5-145">no</span><span class="sxs-lookup"><span data-stu-id="9fdc5-145">no</span></span>        |
| [<span data-ttu-id="9fdc5-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9fdc5-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9fdc5-147">no</span><span class="sxs-lookup"><span data-stu-id="9fdc5-147">no</span></span>        |
| [<span data-ttu-id="9fdc5-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9fdc5-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9fdc5-149">no</span><span class="sxs-lookup"><span data-stu-id="9fdc5-149">no</span></span>        |
| [<span data-ttu-id="9fdc5-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9fdc5-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9fdc5-151">no</span><span class="sxs-lookup"><span data-stu-id="9fdc5-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9fdc5-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9fdc5-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fdc5-153">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9fdc5-153">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





