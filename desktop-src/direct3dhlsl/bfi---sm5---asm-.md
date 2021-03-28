---
title: BFI (SM5-ASM)
description: Dado un intervalo de bits del LSB de un número, coloque el número de bits en otro número en cualquier desplazamiento.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077106"
---
# <a name="bfi-sm5---asm"></a><span data-ttu-id="2398c-103">BFI (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2398c-103">bfi (sm5 - asm)</span></span>

<span data-ttu-id="2398c-104">Dado un intervalo de bits del LSB de un número, coloque el número de bits en otro número en cualquier desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="2398c-104">Given a bit range from the LSB of a number, place that number of bits in another number at any offset.</span></span>



| <span data-ttu-id="2398c-105">BFI dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle \] , src2 \[ . swizzle \] , src3 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2398c-105">bfi dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\], src3\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2398c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2398c-106">Item</span></span>                                                            | <span data-ttu-id="2398c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2398c-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2398c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2398c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2398c-109">\[en \] la dirección de los resultados.</span><span class="sxs-lookup"><span data-stu-id="2398c-109">\[in\] The address of the results.</span></span><br/>                       |
| <span data-ttu-id="2398c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2398c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2398c-111">\[en \] el ancho del campo de bits que se tomará de *src2*.</span><span class="sxs-lookup"><span data-stu-id="2398c-111">\[in\] The bitfield width to take from *src2*.</span></span><br/>           |
| <span data-ttu-id="2398c-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="2398c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2398c-113">\[en \] el desplazamiento de bits para reemplazar bits en *src3*.</span><span class="sxs-lookup"><span data-stu-id="2398c-113">\[in\] The bitfield offset for replacing bits in *src3*.</span></span><br/> |
| <span data-ttu-id="2398c-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="2398c-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="2398c-115">\[en \] el número desde el que se toman los bits.</span><span class="sxs-lookup"><span data-stu-id="2398c-115">\[in\] The number the bits are taken from.</span></span> <br/>              |
| <span data-ttu-id="2398c-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span><span class="sxs-lookup"><span data-stu-id="2398c-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span></span><br/> | <span data-ttu-id="2398c-117">\[en \] el número de bits que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="2398c-117">\[in\] The number with bits to be replaced.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="2398c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2398c-118">Remarks</span></span>

<span data-ttu-id="2398c-119">Los LSB 5 bits de *src0* proporcionan el ancho del campo de bits (0-31) que se va a tomar de *src2*.</span><span class="sxs-lookup"><span data-stu-id="2398c-119">The LSB 5 bits of *src0* provide the bitfield width (0-31) to take from *src2*.</span></span>

<span data-ttu-id="2398c-120">Los 5 bits LSB de *SRC1* proporcionan el desplazamiento de bits de bits (0-31) para empezar a reemplazar los bits en el número leído de *src3*.</span><span class="sxs-lookup"><span data-stu-id="2398c-120">The LSB 5 bits of *src1* provide the bitfield offset (0-31) to start replacing bits in the number read from *src3*.</span></span>

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

<span data-ttu-id="2398c-121">Esta instrucción se usa para empaquetar enteros o marcas.</span><span class="sxs-lookup"><span data-stu-id="2398c-121">This instruction is used for packing integers or flags.</span></span>

<span data-ttu-id="2398c-122">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="2398c-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2398c-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="2398c-123">Vertex</span></span> | <span data-ttu-id="2398c-124">Casco</span><span class="sxs-lookup"><span data-stu-id="2398c-124">Hull</span></span> | <span data-ttu-id="2398c-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="2398c-125">Domain</span></span> | <span data-ttu-id="2398c-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="2398c-126">Geometry</span></span> | <span data-ttu-id="2398c-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="2398c-127">Pixel</span></span> | <span data-ttu-id="2398c-128">Compute</span><span class="sxs-lookup"><span data-stu-id="2398c-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2398c-129">X</span><span class="sxs-lookup"><span data-stu-id="2398c-129">X</span></span>      | <span data-ttu-id="2398c-130">X</span><span class="sxs-lookup"><span data-stu-id="2398c-130">X</span></span>    | <span data-ttu-id="2398c-131">X</span><span class="sxs-lookup"><span data-stu-id="2398c-131">X</span></span>      | <span data-ttu-id="2398c-132">X</span><span class="sxs-lookup"><span data-stu-id="2398c-132">X</span></span>        | <span data-ttu-id="2398c-133">X</span><span class="sxs-lookup"><span data-stu-id="2398c-133">X</span></span>     | <span data-ttu-id="2398c-134">X</span><span class="sxs-lookup"><span data-stu-id="2398c-134">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2398c-135">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2398c-135">Minimum Shader Model</span></span>

<span data-ttu-id="2398c-136">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2398c-136">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2398c-137">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2398c-137">Shader Model</span></span>                                              | <span data-ttu-id="2398c-138">Compatible</span><span class="sxs-lookup"><span data-stu-id="2398c-138">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2398c-139">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2398c-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2398c-140">sí</span><span class="sxs-lookup"><span data-stu-id="2398c-140">yes</span></span>       |
| [<span data-ttu-id="2398c-141">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2398c-141">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2398c-142">no</span><span class="sxs-lookup"><span data-stu-id="2398c-142">no</span></span>        |
| [<span data-ttu-id="2398c-143">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2398c-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2398c-144">no</span><span class="sxs-lookup"><span data-stu-id="2398c-144">no</span></span>        |
| [<span data-ttu-id="2398c-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2398c-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2398c-146">no</span><span class="sxs-lookup"><span data-stu-id="2398c-146">no</span></span>        |
| [<span data-ttu-id="2398c-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2398c-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2398c-148">no</span><span class="sxs-lookup"><span data-stu-id="2398c-148">no</span></span>        |
| [<span data-ttu-id="2398c-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2398c-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2398c-150">no</span><span class="sxs-lookup"><span data-stu-id="2398c-150">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2398c-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2398c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2398c-152">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2398c-152">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





