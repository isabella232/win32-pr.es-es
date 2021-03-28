---
title: llamada (SM4-ASM)
description: Llama a una subrutina marcada por donde aparece la etiqueta l \ en el programa.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dac86fa52140968443f01050cebc57718fea420
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784936"
---
# <a name="call-sm4---asm"></a><span data-ttu-id="5f027-103">llamada (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5f027-103">call (sm4 - asm)</span></span>

<span data-ttu-id="5f027-104">Llama a una subrutina marcada por donde aparece la etiqueta **l \#** en el programa.</span><span class="sxs-lookup"><span data-stu-id="5f027-104">Calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="5f027-105">llamar a l\#</span><span class="sxs-lookup"><span data-stu-id="5f027-105">call l\#</span></span> |
|----------|



 



| <span data-ttu-id="5f027-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f027-106">Item</span></span>                                                       | <span data-ttu-id="5f027-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f027-107">Description</span></span>                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="5f027-108"><span id="l_"></span><span id="L_"></span>*CG\#*</span><span class="sxs-lookup"><span data-stu-id="5f027-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="5f027-109">\[en \] la etiqueta de la subrutina.</span><span class="sxs-lookup"><span data-stu-id="5f027-109">\[in\] The label of the subroutine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5f027-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f027-110">Remarks</span></span>

<span data-ttu-id="5f027-111">Cuando se encuentra un [RET](ret--sm4---asm-.md) , se devuelve la ejecución a la instrucción después de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="5f027-111">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="5f027-112">El formato de token contiene el desplazamiento de la etiqueta correspondiente en el sombreador para mayor comodidad.</span><span class="sxs-lookup"><span data-stu-id="5f027-112">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="5f027-113">En el ejemplo siguiente se muestra la instrucción de llamada.</span><span class="sxs-lookup"><span data-stu-id="5f027-113">The following example shows the call instruction.</span></span>


```
                ...
                call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret
```



### <a name="restrictions"></a><span data-ttu-id="5f027-114">Restricciones</span><span class="sxs-lookup"><span data-stu-id="5f027-114">Restrictions</span></span>

-   <span data-ttu-id="5f027-115">Las subrutinas pueden anidar 32 profundidad.</span><span class="sxs-lookup"><span data-stu-id="5f027-115">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="5f027-116">La pila de direcciones devueltas se administra de forma transparente en la implementación.</span><span class="sxs-lookup"><span data-stu-id="5f027-116">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="5f027-117">Si ya hay 32 entradas en la pila de direcciones devueltas y se emite una **llamada** , se omite la llamada.</span><span class="sxs-lookup"><span data-stu-id="5f027-117">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="5f027-118">No hay ninguna pila de parámetros automática.</span><span class="sxs-lookup"><span data-stu-id="5f027-118">There is no automatic parameter stack.</span></span> <span data-ttu-id="5f027-119">La aplicación puede usar una matriz de registro temporal indexable (x \# \[ \] ) para implementar manualmente una pila.</span><span class="sxs-lookup"><span data-stu-id="5f027-119">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="5f027-120">Sin embargo, las direcciones de devolución de llamada de subrutina no son visibles y son ortogonales a cualquier administración de pila manual realizada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f027-120">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="5f027-121">No se permite la indexación del parámetro *l \#* .</span><span class="sxs-lookup"><span data-stu-id="5f027-121">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="5f027-122">No se permite la recursividad.</span><span class="sxs-lookup"><span data-stu-id="5f027-122">Recursion is not permitted.</span></span>

<span data-ttu-id="5f027-123">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="5f027-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5f027-124">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5f027-124">Vertex Shader</span></span> | <span data-ttu-id="5f027-125">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="5f027-125">Geometry Shader</span></span> | <span data-ttu-id="5f027-126">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5f027-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5f027-127">x</span><span class="sxs-lookup"><span data-stu-id="5f027-127">x</span></span>             | <span data-ttu-id="5f027-128">x</span><span class="sxs-lookup"><span data-stu-id="5f027-128">x</span></span>               | <span data-ttu-id="5f027-129">x</span><span class="sxs-lookup"><span data-stu-id="5f027-129">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5f027-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="5f027-130">Minimum Shader Model</span></span>

<span data-ttu-id="5f027-131">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5f027-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5f027-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="5f027-132">Shader Model</span></span>                                              | <span data-ttu-id="5f027-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="5f027-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5f027-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5f027-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5f027-135">sí</span><span class="sxs-lookup"><span data-stu-id="5f027-135">yes</span></span>       |
| [<span data-ttu-id="5f027-136">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="5f027-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5f027-137">sí</span><span class="sxs-lookup"><span data-stu-id="5f027-137">yes</span></span>       |
| [<span data-ttu-id="5f027-138">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="5f027-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5f027-139">sí</span><span class="sxs-lookup"><span data-stu-id="5f027-139">yes</span></span>       |
| [<span data-ttu-id="5f027-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f027-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5f027-141">no</span><span class="sxs-lookup"><span data-stu-id="5f027-141">no</span></span>        |
| [<span data-ttu-id="5f027-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f027-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5f027-143">no</span><span class="sxs-lookup"><span data-stu-id="5f027-143">no</span></span>        |
| [<span data-ttu-id="5f027-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f027-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5f027-145">no</span><span class="sxs-lookup"><span data-stu-id="5f027-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5f027-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f027-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f027-147">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f027-147">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





