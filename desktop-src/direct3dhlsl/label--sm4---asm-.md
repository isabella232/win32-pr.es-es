---
title: etiqueta (SM4-ASM)
description: Indica el principio de una subrutina.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4c2d73db5d776c75b6d6339cecb7748a9868d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784954"
---
# <a name="label-sm4---asm"></a><span data-ttu-id="928ec-103">etiqueta (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="928ec-103">label (sm4 - asm)</span></span>

<span data-ttu-id="928ec-104">Indica el principio de una subrutina.</span><span class="sxs-lookup"><span data-stu-id="928ec-104">Indicates the beginning of a subroutine.</span></span>



| <span data-ttu-id="928ec-105">etiqueta l\#</span><span class="sxs-lookup"><span data-stu-id="928ec-105">label l\#</span></span> |
|-----------|



 



| <span data-ttu-id="928ec-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="928ec-106">Item</span></span>                                                       | <span data-ttu-id="928ec-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="928ec-107">Description</span></span>                         |
|------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="928ec-108"><span id="l_"></span><span id="L_"></span>*CG\#*</span><span class="sxs-lookup"><span data-stu-id="928ec-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="928ec-109">\[en \] el número de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="928ec-109">\[in\] The label number.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="928ec-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="928ec-110">Remarks</span></span>

<span data-ttu-id="928ec-111">Una **etiqueta** solo puede aparecer directamente después de una instrucción [**RET**](ret--sm4---asm-.md) que no está anidada en las instrucciones de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="928ec-111">A **label** can only appear directly after a [**ret**](ret--sm4---asm-.md) instruction which is not nested in any flow control statements.</span></span>

<span data-ttu-id="928ec-112">El código anterior a la primera **etiqueta** de un programa es el programa principal.</span><span class="sxs-lookup"><span data-stu-id="928ec-112">The code before the first **label** in a program is the main program.</span></span> <span data-ttu-id="928ec-113">Todas las subrutinas aparecen al final del programa, indicadas por las instrucciones de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="928ec-113">All subroutines appear at the end of the program, indicated by **label** statements.</span></span>

<span data-ttu-id="928ec-114">En el ejemplo siguiente se muestra cómo utilizar esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="928ec-114">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
```

<span data-ttu-id="928ec-115">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="928ec-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="928ec-116">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="928ec-116">Vertex Shader</span></span> | <span data-ttu-id="928ec-117">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="928ec-117">Geometry Shader</span></span> | <span data-ttu-id="928ec-118">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="928ec-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="928ec-119">x</span><span class="sxs-lookup"><span data-stu-id="928ec-119">x</span></span>             | <span data-ttu-id="928ec-120">x</span><span class="sxs-lookup"><span data-stu-id="928ec-120">x</span></span>               | <span data-ttu-id="928ec-121">x</span><span class="sxs-lookup"><span data-stu-id="928ec-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="928ec-122">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="928ec-122">Minimum Shader Model</span></span>

<span data-ttu-id="928ec-123">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="928ec-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="928ec-124">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="928ec-124">Shader Model</span></span>                                              | <span data-ttu-id="928ec-125">Compatible</span><span class="sxs-lookup"><span data-stu-id="928ec-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="928ec-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="928ec-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="928ec-127">sí</span><span class="sxs-lookup"><span data-stu-id="928ec-127">yes</span></span>       |
| [<span data-ttu-id="928ec-128">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="928ec-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="928ec-129">sí</span><span class="sxs-lookup"><span data-stu-id="928ec-129">yes</span></span>       |
| [<span data-ttu-id="928ec-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="928ec-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="928ec-131">sí</span><span class="sxs-lookup"><span data-stu-id="928ec-131">yes</span></span>       |
| [<span data-ttu-id="928ec-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="928ec-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="928ec-133">no</span><span class="sxs-lookup"><span data-stu-id="928ec-133">no</span></span>        |
| [<span data-ttu-id="928ec-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="928ec-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="928ec-135">no</span><span class="sxs-lookup"><span data-stu-id="928ec-135">no</span></span>        |
| [<span data-ttu-id="928ec-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="928ec-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="928ec-137">no</span><span class="sxs-lookup"><span data-stu-id="928ec-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="928ec-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="928ec-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="928ec-139">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="928ec-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





