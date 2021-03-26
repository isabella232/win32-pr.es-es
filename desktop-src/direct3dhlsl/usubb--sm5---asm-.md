---
title: usubb (SM5-ASM)
description: Número entero sin signo que se resta con el préstamo.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419891"
---
# <a name="usubb-sm5---asm"></a><span data-ttu-id="9b591-103">usubb (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9b591-103">usubb (sm5 - asm)</span></span>

<span data-ttu-id="9b591-104">Número entero sin signo que se resta con el préstamo.</span><span class="sxs-lookup"><span data-stu-id="9b591-104">Unsigned integer subtract with borrow.</span></span>



| <span data-ttu-id="9b591-105">usubb dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9b591-105">usubb dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="9b591-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="9b591-106">Item</span></span>                                                               | <span data-ttu-id="9b591-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b591-107">Description</span></span>                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b591-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="9b591-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="9b591-109">\[en \] contiene los resultados de LSAB de la instrucción.</span><span class="sxs-lookup"><span data-stu-id="9b591-109">\[in\] Contains the LSAB results of the instruction.</span></span><br/>                                   |
| <span data-ttu-id="9b591-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="9b591-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="9b591-111">\[en \] el componente correspondiente de *dest0* que especifica si se ha producido un préstamo.</span><span class="sxs-lookup"><span data-stu-id="9b591-111">\[in\] The corresponding component of *dest0* that specifies if a borrow was produced.</span></span><br/> |
| <span data-ttu-id="9b591-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9b591-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="9b591-113">\[en \] el valor del que se va a restar.</span><span class="sxs-lookup"><span data-stu-id="9b591-113">\[in\] The value from which to subtract.</span></span><br/>                                               |
| <span data-ttu-id="9b591-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="9b591-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="9b591-115">\[en \] la cantidad que se va a restar de *src0*.</span><span class="sxs-lookup"><span data-stu-id="9b591-115">\[in\] The amount to subtract from *src0*.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="9b591-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b591-116">Remarks</span></span>

<span data-ttu-id="9b591-117">Esta instrucción realiza una resta sin signo de modo de componente de operandos de 32 bits *SRC1* de *src0*, y coloca la parte LSB del resultado de 32 bits en *dest0*.</span><span class="sxs-lookup"><span data-stu-id="9b591-117">This instruction performs a component-wise unsigned subtract of 32-bit operands *src1* from *src0*, placing the LSB part of the 32-bit result in *dest0*.</span></span>

<span data-ttu-id="9b591-118">El componente correspondiente de *dest1* se escribe con 1 si se produce un préstamo; de lo contrario, devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="9b591-118">The corresponding component in *dest1* is written with 1 if a borrow is produced, 0 otherwise.</span></span>

<span data-ttu-id="9b591-119">*dest1* puede ser null si no se necesita el préstamo.</span><span class="sxs-lookup"><span data-stu-id="9b591-119">*dest1* can be NULL if the borrow is not needed.</span></span>

<span data-ttu-id="9b591-120">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="9b591-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9b591-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="9b591-121">Vertex</span></span> | <span data-ttu-id="9b591-122">Casco</span><span class="sxs-lookup"><span data-stu-id="9b591-122">Hull</span></span> | <span data-ttu-id="9b591-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="9b591-123">Domain</span></span> | <span data-ttu-id="9b591-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="9b591-124">Geometry</span></span> | <span data-ttu-id="9b591-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="9b591-125">Pixel</span></span> | <span data-ttu-id="9b591-126">Compute</span><span class="sxs-lookup"><span data-stu-id="9b591-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9b591-127">X</span><span class="sxs-lookup"><span data-stu-id="9b591-127">X</span></span>      | <span data-ttu-id="9b591-128">X</span><span class="sxs-lookup"><span data-stu-id="9b591-128">X</span></span>    | <span data-ttu-id="9b591-129">X</span><span class="sxs-lookup"><span data-stu-id="9b591-129">X</span></span>      | <span data-ttu-id="9b591-130">X</span><span class="sxs-lookup"><span data-stu-id="9b591-130">X</span></span>        | <span data-ttu-id="9b591-131">X</span><span class="sxs-lookup"><span data-stu-id="9b591-131">X</span></span>     | <span data-ttu-id="9b591-132">X</span><span class="sxs-lookup"><span data-stu-id="9b591-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9b591-133">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="9b591-133">Minimum Shader Model</span></span>

<span data-ttu-id="9b591-134">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9b591-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9b591-135">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="9b591-135">Shader Model</span></span>                                              | <span data-ttu-id="9b591-136">Compatible</span><span class="sxs-lookup"><span data-stu-id="9b591-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9b591-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9b591-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9b591-138">sí</span><span class="sxs-lookup"><span data-stu-id="9b591-138">yes</span></span>       |
| [<span data-ttu-id="9b591-139">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="9b591-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9b591-140">no</span><span class="sxs-lookup"><span data-stu-id="9b591-140">no</span></span>        |
| [<span data-ttu-id="9b591-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9b591-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9b591-142">no</span><span class="sxs-lookup"><span data-stu-id="9b591-142">no</span></span>        |
| [<span data-ttu-id="9b591-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b591-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9b591-144">no</span><span class="sxs-lookup"><span data-stu-id="9b591-144">no</span></span>        |
| [<span data-ttu-id="9b591-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b591-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9b591-146">no</span><span class="sxs-lookup"><span data-stu-id="9b591-146">no</span></span>        |
| [<span data-ttu-id="9b591-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b591-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9b591-148">no</span><span class="sxs-lookup"><span data-stu-id="9b591-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9b591-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b591-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b591-150">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b591-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





