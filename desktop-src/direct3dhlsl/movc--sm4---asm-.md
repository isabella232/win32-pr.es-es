---
title: MOVC (SM4-ASM)
description: Movimiento condicional por componente. | MOVC (SM4-ASM)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3116b7bc13102386c57c9b8c63d3534147a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998105"
---
# <a name="movc-sm4---asm"></a><span data-ttu-id="81e6a-104">MOVC (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="81e6a-104">movc (sm4 - asm)</span></span>

<span data-ttu-id="81e6a-105">Movimiento condicional por componente.</span><span class="sxs-lookup"><span data-stu-id="81e6a-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="81e6a-106">MOVC \[ \_ SAT \] dest \[ . Mask \] , src0 \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="81e6a-106">movc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="81e6a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="81e6a-107">Item</span></span>                                                            | <span data-ttu-id="81e6a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="81e6a-108">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e6a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="81e6a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="81e6a-110">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="81e6a-110">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="81e6a-111">Si *src0*, *dest*  =  *SRC1* else *dest*  =  *src2*</span><span class="sxs-lookup"><span data-stu-id="81e6a-111">If *src0*, then *dest* = *src1* else *dest* = *src2*</span></span><br/> |
| <span data-ttu-id="81e6a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="81e6a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="81e6a-113">\[en \] los componentes en los que se va a probar la condición.</span><span class="sxs-lookup"><span data-stu-id="81e6a-113">\[in\] The components on which to test the condition.</span></span><br/>                                                               |
| <span data-ttu-id="81e6a-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="81e6a-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="81e6a-115">\[en \] los componentes que se van a trasladar.</span><span class="sxs-lookup"><span data-stu-id="81e6a-115">\[in\] The components to move.</span></span> <br/>                                                                                     |
| <span data-ttu-id="81e6a-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="81e6a-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="81e6a-117">\[en \] los componentes que se van a trasladar.</span><span class="sxs-lookup"><span data-stu-id="81e6a-117">\[in\] The components to move.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="81e6a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81e6a-118">Remarks</span></span>

<span data-ttu-id="81e6a-119">En el ejemplo siguiente se muestra cómo utilizar esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="81e6a-119">The following example shows how to use this instruction.</span></span>

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

<span data-ttu-id="81e6a-120">Los modificadores de *SRC1* y *src2*, excepto swizzle, suponen que los datos son de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="81e6a-120">The modifiers on *src1* and *src2*, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="81e6a-121">La ausencia de modificadores solo mueve los datos sin modificar los bits.</span><span class="sxs-lookup"><span data-stu-id="81e6a-121">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="81e6a-122">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="81e6a-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="81e6a-123">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="81e6a-123">Vertex Shader</span></span> | <span data-ttu-id="81e6a-124">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="81e6a-124">Geometry Shader</span></span> | <span data-ttu-id="81e6a-125">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="81e6a-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="81e6a-126">x</span><span class="sxs-lookup"><span data-stu-id="81e6a-126">x</span></span>             | <span data-ttu-id="81e6a-127">x</span><span class="sxs-lookup"><span data-stu-id="81e6a-127">x</span></span>               | <span data-ttu-id="81e6a-128">x</span><span class="sxs-lookup"><span data-stu-id="81e6a-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="81e6a-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="81e6a-129">Minimum Shader Model</span></span>

<span data-ttu-id="81e6a-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="81e6a-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="81e6a-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="81e6a-131">Shader Model</span></span>                                              | <span data-ttu-id="81e6a-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="81e6a-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="81e6a-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="81e6a-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="81e6a-134">sí</span><span class="sxs-lookup"><span data-stu-id="81e6a-134">yes</span></span>       |
| [<span data-ttu-id="81e6a-135">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="81e6a-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="81e6a-136">sí</span><span class="sxs-lookup"><span data-stu-id="81e6a-136">yes</span></span>       |
| [<span data-ttu-id="81e6a-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="81e6a-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="81e6a-138">sí</span><span class="sxs-lookup"><span data-stu-id="81e6a-138">yes</span></span>       |
| [<span data-ttu-id="81e6a-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="81e6a-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="81e6a-140">no</span><span class="sxs-lookup"><span data-stu-id="81e6a-140">no</span></span>        |
| [<span data-ttu-id="81e6a-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="81e6a-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="81e6a-142">no</span><span class="sxs-lookup"><span data-stu-id="81e6a-142">no</span></span>        |
| [<span data-ttu-id="81e6a-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="81e6a-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="81e6a-144">no</span><span class="sxs-lookup"><span data-stu-id="81e6a-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="81e6a-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81e6a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81e6a-146">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="81e6a-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





