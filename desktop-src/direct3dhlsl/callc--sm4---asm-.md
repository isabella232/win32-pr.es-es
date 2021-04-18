---
title: callc (SM4-ASM)
description: Llama condicionalmente a una subrutina marcada por donde aparece la etiqueta l \ en el programa.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6bc8c9d1e4a99ce25f99253518482181cdb74d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996904"
---
# <a name="callc-sm4---asm"></a><span data-ttu-id="74b41-103">callc (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="74b41-103">callc (sm4 - asm)</span></span>

<span data-ttu-id="74b41-104">Llama condicionalmente a una subrutina marcada por donde aparece la etiqueta **l \#** en el programa.</span><span class="sxs-lookup"><span data-stu-id="74b41-104">Conditionally calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="74b41-105">callc { \_ z </span><span class="sxs-lookup"><span data-stu-id="74b41-105">callc{\_z</span></span>\|<span data-ttu-id="74b41-106">\_NZ} src0. Select \_ (componente), l\#</span><span class="sxs-lookup"><span data-stu-id="74b41-106">\_nz} src0.select\_component, l\#</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="74b41-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="74b41-107">Item</span></span>                                                            | <span data-ttu-id="74b41-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="74b41-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="74b41-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="74b41-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="74b41-110">\[en \] el componente en el que se va a probar la condición.</span><span class="sxs-lookup"><span data-stu-id="74b41-110">\[in\] The component on which to test the condition.</span></span><br/> |
| <span data-ttu-id="74b41-111"><span id="l_"></span><span id="L_"></span>*CG\#*</span><span class="sxs-lookup"><span data-stu-id="74b41-111"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/>      | <span data-ttu-id="74b41-112">\[en \] la etiqueta de la subrutina.</span><span class="sxs-lookup"><span data-stu-id="74b41-112">\[in\] The label of the subroutine.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="74b41-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74b41-113">Remarks</span></span>

<span data-ttu-id="74b41-114">Cuando se encuentra un [RET](ret--sm4---asm-.md) , se devuelve la ejecución a la instrucción después de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="74b41-114">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="74b41-115">El formato de token contiene el desplazamiento de la etiqueta correspondiente en el sombreador para mayor comodidad.</span><span class="sxs-lookup"><span data-stu-id="74b41-115">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="74b41-116">En el ejemplo siguiente se muestra la instrucción de llamada.</span><span class="sxs-lookup"><span data-stu-id="74b41-116">The following example shows the call instruction.</span></span>


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret

```



### <a name="restrictions"></a><span data-ttu-id="74b41-117">Restricciones</span><span class="sxs-lookup"><span data-stu-id="74b41-117">Restrictions</span></span>

-   <span data-ttu-id="74b41-118">Las subrutinas pueden anidar 32 profundidad.</span><span class="sxs-lookup"><span data-stu-id="74b41-118">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="74b41-119">La pila de direcciones devueltas se administra de forma transparente en la implementación.</span><span class="sxs-lookup"><span data-stu-id="74b41-119">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="74b41-120">Si ya hay 32 entradas en la pila de direcciones devueltas y se emite una **llamada** , se omite la llamada.</span><span class="sxs-lookup"><span data-stu-id="74b41-120">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="74b41-121">No hay ninguna pila de parámetros automática.</span><span class="sxs-lookup"><span data-stu-id="74b41-121">There is no automatic parameter stack.</span></span> <span data-ttu-id="74b41-122">La aplicación puede usar una matriz de registro temporal indexable (x \# \[ \] ) para implementar manualmente una pila.</span><span class="sxs-lookup"><span data-stu-id="74b41-122">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="74b41-123">Sin embargo, las direcciones de devolución de llamada de subrutina no son visibles y son ortogonales a cualquier administración de pila manual realizada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74b41-123">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="74b41-124">No se permite la indexación del parámetro *l \#* .</span><span class="sxs-lookup"><span data-stu-id="74b41-124">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="74b41-125">El registro de 32 bits proporcionado por *src0* se prueba en un nivel de bits.</span><span class="sxs-lookup"><span data-stu-id="74b41-125">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="74b41-126">Si algún bit es distinto de cero, **callc \_ NZ** realizará la llamada.</span><span class="sxs-lookup"><span data-stu-id="74b41-126">If any bit is nonzero, **callc\_nz** will perform the call.</span></span> <span data-ttu-id="74b41-127">Si todos los bits son cero, **callc \_ z** realizará la llamada.</span><span class="sxs-lookup"><span data-stu-id="74b41-127">If all bits are zero, **callc\_z** will perform the call.</span></span>
-   <span data-ttu-id="74b41-128">No se permite la recursividad.</span><span class="sxs-lookup"><span data-stu-id="74b41-128">Recursion is not permitted.</span></span>

<span data-ttu-id="74b41-129">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="74b41-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="74b41-130">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="74b41-130">Vertex Shader</span></span> | <span data-ttu-id="74b41-131">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="74b41-131">Geometry Shader</span></span> | <span data-ttu-id="74b41-132">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="74b41-132">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="74b41-133">x</span><span class="sxs-lookup"><span data-stu-id="74b41-133">x</span></span>             | <span data-ttu-id="74b41-134">x</span><span class="sxs-lookup"><span data-stu-id="74b41-134">x</span></span>               | <span data-ttu-id="74b41-135">x</span><span class="sxs-lookup"><span data-stu-id="74b41-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="74b41-136">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="74b41-136">Minimum Shader Model</span></span>

<span data-ttu-id="74b41-137">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="74b41-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="74b41-138">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="74b41-138">Shader Model</span></span>                                              | <span data-ttu-id="74b41-139">Compatible</span><span class="sxs-lookup"><span data-stu-id="74b41-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="74b41-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="74b41-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="74b41-141">sí</span><span class="sxs-lookup"><span data-stu-id="74b41-141">yes</span></span>       |
| [<span data-ttu-id="74b41-142">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="74b41-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="74b41-143">sí</span><span class="sxs-lookup"><span data-stu-id="74b41-143">yes</span></span>       |
| [<span data-ttu-id="74b41-144">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="74b41-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="74b41-145">sí</span><span class="sxs-lookup"><span data-stu-id="74b41-145">yes</span></span>       |
| [<span data-ttu-id="74b41-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74b41-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="74b41-147">no</span><span class="sxs-lookup"><span data-stu-id="74b41-147">no</span></span>        |
| [<span data-ttu-id="74b41-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74b41-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="74b41-149">no</span><span class="sxs-lookup"><span data-stu-id="74b41-149">no</span></span>        |
| [<span data-ttu-id="74b41-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74b41-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="74b41-151">no</span><span class="sxs-lookup"><span data-stu-id="74b41-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="74b41-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74b41-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74b41-153">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74b41-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





