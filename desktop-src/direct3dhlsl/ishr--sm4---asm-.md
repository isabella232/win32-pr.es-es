---
title: ISHR (SM4-ASM)
description: Desplazamiento aritmético a la derecha (signo de extensión). | ISHR (SM4-ASM)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516543c5501ed886c5c1fa98d093062e3099a0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998245"
---
# <a name="ishr-sm4---asm"></a><span data-ttu-id="6978a-104">ISHR (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6978a-104">ishr (sm4 - asm)</span></span>

<span data-ttu-id="6978a-105">Desplazamiento aritmético a la derecha (signo de extensión).</span><span class="sxs-lookup"><span data-stu-id="6978a-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="6978a-106">ISHR dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="6978a-106">ishr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="6978a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6978a-107">Item</span></span>                                                            | <span data-ttu-id="6978a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6978a-108">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6978a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6978a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6978a-110">\[en \] contiene el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="6978a-110">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="6978a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6978a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6978a-112">\[en \] contiene el valor que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="6978a-112">\[in\] Contains the value to be shifted.</span></span><br/>     |
| <span data-ttu-id="6978a-113"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="6978a-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6978a-114">\[en \] contiene la cantidad de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="6978a-114">\[in\] Contains the shift amount.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="6978a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6978a-115">Remarks</span></span>

<span data-ttu-id="6978a-116">Esta instrucción realiza un cambio aritmético en forma de componente de cada valor de 32 bits de *src0* a la derecha por un recuento de bits sin signo proporcionado por el LSB 5 bits (intervalo 0-31) del *\_ componente SRC1. Select*, replicando el valor de bit 31.</span><span class="sxs-lookup"><span data-stu-id="6978a-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, replicating the value of bit 31.</span></span> <span data-ttu-id="6978a-117">El resultado de 32 bits por componente se coloca en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="6978a-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="6978a-118">El recuento es un valor escalar que se aplica a todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="6978a-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="6978a-119">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="6978a-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6978a-120">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="6978a-120">Vertex Shader</span></span> | <span data-ttu-id="6978a-121">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="6978a-121">Geometry Shader</span></span> | <span data-ttu-id="6978a-122">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="6978a-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6978a-123">x</span><span class="sxs-lookup"><span data-stu-id="6978a-123">x</span></span>             | <span data-ttu-id="6978a-124">x</span><span class="sxs-lookup"><span data-stu-id="6978a-124">x</span></span>               | <span data-ttu-id="6978a-125">x</span><span class="sxs-lookup"><span data-stu-id="6978a-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6978a-126">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="6978a-126">Minimum Shader Model</span></span>

<span data-ttu-id="6978a-127">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6978a-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6978a-128">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="6978a-128">Shader Model</span></span>                                              | <span data-ttu-id="6978a-129">Compatible</span><span class="sxs-lookup"><span data-stu-id="6978a-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6978a-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6978a-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6978a-131">sí</span><span class="sxs-lookup"><span data-stu-id="6978a-131">yes</span></span>       |
| [<span data-ttu-id="6978a-132">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6978a-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6978a-133">sí</span><span class="sxs-lookup"><span data-stu-id="6978a-133">yes</span></span>       |
| [<span data-ttu-id="6978a-134">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6978a-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6978a-135">sí</span><span class="sxs-lookup"><span data-stu-id="6978a-135">yes</span></span>       |
| [<span data-ttu-id="6978a-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6978a-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6978a-137">no</span><span class="sxs-lookup"><span data-stu-id="6978a-137">no</span></span>        |
| [<span data-ttu-id="6978a-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6978a-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6978a-139">no</span><span class="sxs-lookup"><span data-stu-id="6978a-139">no</span></span>        |
| [<span data-ttu-id="6978a-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6978a-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6978a-141">no</span><span class="sxs-lookup"><span data-stu-id="6978a-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6978a-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6978a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6978a-143">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6978a-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





