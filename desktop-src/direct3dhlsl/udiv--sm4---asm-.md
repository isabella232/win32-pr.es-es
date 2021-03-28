---
title: UDIV (SM4-ASM)
description: División de enteros sin signo.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a3dd2f4170a3c8fe522af12d412cfae49396da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419929"
---
# <a name="udiv-sm4---asm"></a><span data-ttu-id="ce0a4-103">UDIV (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ce0a4-103">udiv (sm4 - asm)</span></span>

<span data-ttu-id="ce0a4-104">División de enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="ce0a4-104">Unsigned integer divide.</span></span>



| <span data-ttu-id="ce0a4-105">UDIV destQUOT \[ . Mask \] , destREM \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ce0a4-105">udiv destQUOT\[.mask\], destREM\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="ce0a4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ce0a4-106">Item</span></span>                                                                                                   | <span data-ttu-id="ce0a4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce0a4-107">Description</span></span>                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ce0a4-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span><span class="sxs-lookup"><span data-stu-id="ce0a4-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span></span><br/> | <span data-ttu-id="ce0a4-109">\[en \] la dirección del cociente resultante.</span><span class="sxs-lookup"><span data-stu-id="ce0a4-109">\[in\] The address of the resulting quotient.</span></span><br/>   |
| <span data-ttu-id="ce0a4-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span><span class="sxs-lookup"><span data-stu-id="ce0a4-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span></span><br/>     | <span data-ttu-id="ce0a4-111">\[en \] la dirección del resto resultante.</span><span class="sxs-lookup"><span data-stu-id="ce0a4-111">\[in\] The address of the resulting remainder.</span></span><br/>  |
| <span data-ttu-id="ce0a4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ce0a4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                        | <span data-ttu-id="ce0a4-113">\[en \] los componentes que se van a dividir por *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="ce0a4-113">\[in\] The components to be divided by *src1*.</span></span><br/>  |
| <span data-ttu-id="ce0a4-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="ce0a4-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                        | <span data-ttu-id="ce0a4-115">\[en \] los componentes de whch para dividir *src0*.</span><span class="sxs-lookup"><span data-stu-id="ce0a4-115">\[in\] The components by whch to divide *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce0a4-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce0a4-116">Remarks</span></span>

<span data-ttu-id="ce0a4-117">Esta instrucción realiza una división sin signo de modo de componente del operando de 32 bits *src0* por el operando de 32 bits *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="ce0a4-117">This instruction performs a component-wise unsigned divide of the 32-bit operand *src0* by the 32-bit operand *src1*.</span></span> <span data-ttu-id="ce0a4-118">Los resultados de las divisiones son los cocientes de 32 bits colocados en *destQUOT* y los restos de 32 bits colocados en *destREM*.</span><span class="sxs-lookup"><span data-stu-id="ce0a4-118">The results of the divides are the 32-bit quotients placed in *destQUOT* and 32-bit remainders placed in *destREM*.</span></span>

<span data-ttu-id="ce0a4-119">La división por cero devuelve 0xFFFFFFFF para el cociente y el resto.</span><span class="sxs-lookup"><span data-stu-id="ce0a4-119">Divide by zero returns 0xffffffff for both quotient and remainder.</span></span>

<span data-ttu-id="ce0a4-120">Puede especificar *destQUOT* o *destREM* como null en lugar de especificar un registro, si no se necesita el cociente o el resto.</span><span class="sxs-lookup"><span data-stu-id="ce0a4-120">You can specifiy either *destQUOT* or *destREM* as NULL instead of specifying a register, if the quotient or remainder are not needed.</span></span>

<span data-ttu-id="ce0a4-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ce0a4-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ce0a4-122">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ce0a4-122">Vertex Shader</span></span> | <span data-ttu-id="ce0a4-123">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="ce0a4-123">Geometry Shader</span></span> | <span data-ttu-id="ce0a4-124">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ce0a4-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ce0a4-125">x</span><span class="sxs-lookup"><span data-stu-id="ce0a4-125">x</span></span>             | <span data-ttu-id="ce0a4-126">x</span><span class="sxs-lookup"><span data-stu-id="ce0a4-126">x</span></span>               | <span data-ttu-id="ce0a4-127">x</span><span class="sxs-lookup"><span data-stu-id="ce0a4-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ce0a4-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ce0a4-128">Minimum Shader Model</span></span>

<span data-ttu-id="ce0a4-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ce0a4-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ce0a4-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ce0a4-130">Shader Model</span></span>                                              | <span data-ttu-id="ce0a4-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="ce0a4-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ce0a4-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ce0a4-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ce0a4-133">sí</span><span class="sxs-lookup"><span data-stu-id="ce0a4-133">yes</span></span>       |
| [<span data-ttu-id="ce0a4-134">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ce0a4-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ce0a4-135">sí</span><span class="sxs-lookup"><span data-stu-id="ce0a4-135">yes</span></span>       |
| [<span data-ttu-id="ce0a4-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ce0a4-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ce0a4-137">sí</span><span class="sxs-lookup"><span data-stu-id="ce0a4-137">yes</span></span>       |
| [<span data-ttu-id="ce0a4-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce0a4-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ce0a4-139">no</span><span class="sxs-lookup"><span data-stu-id="ce0a4-139">no</span></span>        |
| [<span data-ttu-id="ce0a4-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce0a4-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ce0a4-141">no</span><span class="sxs-lookup"><span data-stu-id="ce0a4-141">no</span></span>        |
| [<span data-ttu-id="ce0a4-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce0a4-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ce0a4-143">no</span><span class="sxs-lookup"><span data-stu-id="ce0a4-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ce0a4-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce0a4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce0a4-145">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce0a4-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





