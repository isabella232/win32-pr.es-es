---
title: ushr (SM5-ASM)
description: Desplazar a la derecha. | ushr (SM5-ASM)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33c627ec4aa985b5ac8a27cf0babd6219c9247c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986503"
---
# <a name="ushr-sm5---asm"></a><span data-ttu-id="12187-104">ushr (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="12187-104">ushr (sm5 - asm)</span></span>

<span data-ttu-id="12187-105">Desplazar a la derecha.</span><span class="sxs-lookup"><span data-stu-id="12187-105">Shift right.</span></span>



| <span data-ttu-id="12187-106">ubfe dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="12187-106">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="12187-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="12187-107">Item</span></span>                                                            | <span data-ttu-id="12187-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="12187-108">Description</span></span>                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="12187-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="12187-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="12187-110">\[en \] contiene los resultados de la instrucción.</span><span class="sxs-lookup"><span data-stu-id="12187-110">\[in\] Contains the results of the instruction.</span></span><br/>                   |
| <span data-ttu-id="12187-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="12187-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="12187-112">\[en \] los valores de 32 bits que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="12187-112">\[in\] The 32-bit values to shift.</span></span><br/>                                |
| <span data-ttu-id="12187-113"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="12187-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="12187-114">\[en \] los 5 bits de LSB, proporcione el número de bits que se van a desplazar (0-31).</span><span class="sxs-lookup"><span data-stu-id="12187-114">\[in\] The LSB 5 bits provide the number of bits to shift (0-31).</span></span><br/> |



 

<span data-ttu-id="12187-115">Esta instrucción realiza un desplazamiento por componentes de cada valor de 32 bits de *src0* a la derecha un recuento de bits sin signo proporcionado por el LSB 5 bits (intervalo 0-31) en *SRC1*, insertando 0.</span><span class="sxs-lookup"><span data-stu-id="12187-115">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="12187-116">Los resultados de 32 bits por componente se colocan en *dest*.</span><span class="sxs-lookup"><span data-stu-id="12187-116">The 32-bit per component results is placed in *dest*.</span></span>

<span data-ttu-id="12187-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="12187-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="12187-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="12187-118">Vertex</span></span> | <span data-ttu-id="12187-119">Casco</span><span class="sxs-lookup"><span data-stu-id="12187-119">Hull</span></span> | <span data-ttu-id="12187-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="12187-120">Domain</span></span> | <span data-ttu-id="12187-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="12187-121">Geometry</span></span> | <span data-ttu-id="12187-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="12187-122">Pixel</span></span> | <span data-ttu-id="12187-123">Compute</span><span class="sxs-lookup"><span data-stu-id="12187-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="12187-124">X</span><span class="sxs-lookup"><span data-stu-id="12187-124">X</span></span>      | <span data-ttu-id="12187-125">X</span><span class="sxs-lookup"><span data-stu-id="12187-125">X</span></span>    | <span data-ttu-id="12187-126">X</span><span class="sxs-lookup"><span data-stu-id="12187-126">X</span></span>      | <span data-ttu-id="12187-127">X</span><span class="sxs-lookup"><span data-stu-id="12187-127">X</span></span>        | <span data-ttu-id="12187-128">X</span><span class="sxs-lookup"><span data-stu-id="12187-128">X</span></span>     | <span data-ttu-id="12187-129">X</span><span class="sxs-lookup"><span data-stu-id="12187-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="12187-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="12187-130">Minimum Shader Model</span></span>

<span data-ttu-id="12187-131">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="12187-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="12187-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="12187-132">Shader Model</span></span>                                              | <span data-ttu-id="12187-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="12187-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="12187-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="12187-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="12187-135">sí</span><span class="sxs-lookup"><span data-stu-id="12187-135">yes</span></span>       |
| [<span data-ttu-id="12187-136">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="12187-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="12187-137">no</span><span class="sxs-lookup"><span data-stu-id="12187-137">no</span></span>        |
| [<span data-ttu-id="12187-138">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="12187-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="12187-139">no</span><span class="sxs-lookup"><span data-stu-id="12187-139">no</span></span>        |
| [<span data-ttu-id="12187-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12187-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="12187-141">no</span><span class="sxs-lookup"><span data-stu-id="12187-141">no</span></span>        |
| [<span data-ttu-id="12187-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12187-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="12187-143">no</span><span class="sxs-lookup"><span data-stu-id="12187-143">no</span></span>        |
| [<span data-ttu-id="12187-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12187-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="12187-145">no</span><span class="sxs-lookup"><span data-stu-id="12187-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="12187-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12187-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12187-147">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12187-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





