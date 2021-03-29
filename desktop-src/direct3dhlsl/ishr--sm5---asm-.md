---
title: ISHR (SM5-ASM)
description: Desplazamiento aritmético a la derecha (signo de extensión). | ISHR (SM5-ASM)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998244"
---
# <a name="ishr-sm5---asm"></a><span data-ttu-id="2b22f-104">ISHR (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2b22f-104">ishr (sm5 - asm)</span></span>

<span data-ttu-id="2b22f-105">Desplazamiento aritmético a la derecha (signo de extensión).</span><span class="sxs-lookup"><span data-stu-id="2b22f-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="2b22f-106">ishl dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2b22f-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="2b22f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="2b22f-107">Item</span></span>                                                            | <span data-ttu-id="2b22f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b22f-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2b22f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2b22f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2b22f-110">\[en \] contiene los resultados del desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="2b22f-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="2b22f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2b22f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2b22f-112">\[en \] el número de bits que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="2b22f-112">\[in\] The number of bits to shift.</span></span><br/>       |
| <span data-ttu-id="2b22f-113"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="2b22f-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2b22f-114">\[en \] los valores de 32 bits que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="2b22f-114">\[in\] The 32-bit values to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="2b22f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b22f-115">Remarks</span></span>

<span data-ttu-id="2b22f-116">Esta instrucción realiza un cambio aritmético de modo de componente de cada valor de 32 bits de *src0* a la derecha por un recuento de bits sin signo proporcionado por el LSB 5 bits (intervalo 0-31) en *SRC1*, replicando el valor de bit 31.</span><span class="sxs-lookup"><span data-stu-id="2b22f-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, replicating the value of bit 31.</span></span> <span data-ttu-id="2b22f-117">El resultado de 32 bits por componente se coloca en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="2b22f-117">The 32-bit per component result is placed in *dest*.</span></span>

<span data-ttu-id="2b22f-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="2b22f-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2b22f-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="2b22f-119">Vertex</span></span> | <span data-ttu-id="2b22f-120">Casco</span><span class="sxs-lookup"><span data-stu-id="2b22f-120">Hull</span></span> | <span data-ttu-id="2b22f-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="2b22f-121">Domain</span></span> | <span data-ttu-id="2b22f-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="2b22f-122">Geometry</span></span> | <span data-ttu-id="2b22f-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="2b22f-123">Pixel</span></span> | <span data-ttu-id="2b22f-124">Compute</span><span class="sxs-lookup"><span data-stu-id="2b22f-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2b22f-125">X</span><span class="sxs-lookup"><span data-stu-id="2b22f-125">X</span></span>      | <span data-ttu-id="2b22f-126">X</span><span class="sxs-lookup"><span data-stu-id="2b22f-126">X</span></span>    | <span data-ttu-id="2b22f-127">X</span><span class="sxs-lookup"><span data-stu-id="2b22f-127">X</span></span>      | <span data-ttu-id="2b22f-128">X</span><span class="sxs-lookup"><span data-stu-id="2b22f-128">X</span></span>        | <span data-ttu-id="2b22f-129">X</span><span class="sxs-lookup"><span data-stu-id="2b22f-129">X</span></span>     | <span data-ttu-id="2b22f-130">X</span><span class="sxs-lookup"><span data-stu-id="2b22f-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2b22f-131">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2b22f-131">Minimum Shader Model</span></span>

<span data-ttu-id="2b22f-132">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2b22f-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2b22f-133">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2b22f-133">Shader Model</span></span>                                              | <span data-ttu-id="2b22f-134">Compatible</span><span class="sxs-lookup"><span data-stu-id="2b22f-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2b22f-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2b22f-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2b22f-136">sí</span><span class="sxs-lookup"><span data-stu-id="2b22f-136">yes</span></span>       |
| [<span data-ttu-id="2b22f-137">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2b22f-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2b22f-138">no</span><span class="sxs-lookup"><span data-stu-id="2b22f-138">no</span></span>        |
| [<span data-ttu-id="2b22f-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2b22f-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2b22f-140">no</span><span class="sxs-lookup"><span data-stu-id="2b22f-140">no</span></span>        |
| [<span data-ttu-id="2b22f-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b22f-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2b22f-142">no</span><span class="sxs-lookup"><span data-stu-id="2b22f-142">no</span></span>        |
| [<span data-ttu-id="2b22f-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b22f-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2b22f-144">no</span><span class="sxs-lookup"><span data-stu-id="2b22f-144">no</span></span>        |
| [<span data-ttu-id="2b22f-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b22f-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2b22f-146">no</span><span class="sxs-lookup"><span data-stu-id="2b22f-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2b22f-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b22f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b22f-148">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b22f-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





