---
title: uaddc (SM5-ASM)
description: Entero sin signo agregar con transporte.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f57f75be617e32c15212207110851520a7a281e2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532866"
---
# <a name="uaddc-sm5---asm"></a><span data-ttu-id="0fe09-103">uaddc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0fe09-103">uaddc (sm5 - asm)</span></span>

<span data-ttu-id="0fe09-104">Entero sin signo agregar con transporte.</span><span class="sxs-lookup"><span data-stu-id="0fe09-104">Unsigned integer add with carry.</span></span>



| <span data-ttu-id="0fe09-105">uaddc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0fe09-105">uaddc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="0fe09-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="0fe09-106">Item</span></span>                                                               | <span data-ttu-id="0fe09-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fe09-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="0fe09-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="0fe09-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="0fe09-109">\[en \] la dirección del resultado.</span><span class="sxs-lookup"><span data-stu-id="0fe09-109">\[in\] Address of the result.</span></span><br/>               |
| <span data-ttu-id="0fe09-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="0fe09-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="0fe09-111">\[en \] 1 si se produce el transporte.</span><span class="sxs-lookup"><span data-stu-id="0fe09-111">\[in\] 1 if carry is produced.</span></span> <span data-ttu-id="0fe09-112">De lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="0fe09-112">Otherwise 0.</span></span><br/> |
| <span data-ttu-id="0fe09-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0fe09-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="0fe09-114">\[en \] el operando de 32 bits que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="0fe09-114">\[in\] 32-bit operand to be added.</span></span><br/>          |
| <span data-ttu-id="0fe09-115"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="0fe09-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="0fe09-116">\[en \] el operando de 32 bits que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="0fe09-116">\[in\] 32-bit operand to be added.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="0fe09-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fe09-117">Remarks</span></span>

<span data-ttu-id="0fe09-118">*dest1* puede ser null si no se necesita el transporte.</span><span class="sxs-lookup"><span data-stu-id="0fe09-118">*dest1* can be NULL if the carry is not needed.</span></span>

<span data-ttu-id="0fe09-119">Use esta instrucción para la aritmética de alta precisión.</span><span class="sxs-lookup"><span data-stu-id="0fe09-119">Use this instruction for high precision arithmetic.</span></span>

<span data-ttu-id="0fe09-120">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="0fe09-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0fe09-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="0fe09-121">Vertex</span></span> | <span data-ttu-id="0fe09-122">Casco</span><span class="sxs-lookup"><span data-stu-id="0fe09-122">Hull</span></span> | <span data-ttu-id="0fe09-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="0fe09-123">Domain</span></span> | <span data-ttu-id="0fe09-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="0fe09-124">Geometry</span></span> | <span data-ttu-id="0fe09-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="0fe09-125">Pixel</span></span> | <span data-ttu-id="0fe09-126">Compute</span><span class="sxs-lookup"><span data-stu-id="0fe09-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0fe09-127">X</span><span class="sxs-lookup"><span data-stu-id="0fe09-127">X</span></span>      | <span data-ttu-id="0fe09-128">X</span><span class="sxs-lookup"><span data-stu-id="0fe09-128">X</span></span>    | <span data-ttu-id="0fe09-129">X</span><span class="sxs-lookup"><span data-stu-id="0fe09-129">X</span></span>      | <span data-ttu-id="0fe09-130">X</span><span class="sxs-lookup"><span data-stu-id="0fe09-130">X</span></span>        | <span data-ttu-id="0fe09-131">X</span><span class="sxs-lookup"><span data-stu-id="0fe09-131">X</span></span>     | <span data-ttu-id="0fe09-132">X</span><span class="sxs-lookup"><span data-stu-id="0fe09-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0fe09-133">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0fe09-133">Minimum Shader Model</span></span>

<span data-ttu-id="0fe09-134">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0fe09-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0fe09-135">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0fe09-135">Shader Model</span></span>                                              | <span data-ttu-id="0fe09-136">Compatible</span><span class="sxs-lookup"><span data-stu-id="0fe09-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0fe09-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0fe09-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0fe09-138">sí</span><span class="sxs-lookup"><span data-stu-id="0fe09-138">yes</span></span>       |
| [<span data-ttu-id="0fe09-139">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="0fe09-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0fe09-140">no</span><span class="sxs-lookup"><span data-stu-id="0fe09-140">no</span></span>        |
| [<span data-ttu-id="0fe09-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0fe09-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0fe09-142">no</span><span class="sxs-lookup"><span data-stu-id="0fe09-142">no</span></span>        |
| [<span data-ttu-id="0fe09-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fe09-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0fe09-144">no</span><span class="sxs-lookup"><span data-stu-id="0fe09-144">no</span></span>        |
| [<span data-ttu-id="0fe09-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fe09-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0fe09-146">no</span><span class="sxs-lookup"><span data-stu-id="0fe09-146">no</span></span>        |
| [<span data-ttu-id="0fe09-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fe09-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0fe09-148">no</span><span class="sxs-lookup"><span data-stu-id="0fe09-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0fe09-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0fe09-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fe09-150">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fe09-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





