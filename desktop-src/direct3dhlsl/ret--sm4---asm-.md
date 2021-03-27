---
title: RET (SM4-ASM)
description: Instrucción return.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d834cd9f32d6e38f40666ab235f705c0fc80513f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784918"
---
# <a name="ret-sm4---asm"></a><span data-ttu-id="ce696-103">RET (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ce696-103">ret (sm4 - asm)</span></span>

<span data-ttu-id="ce696-104">Instrucción return.</span><span class="sxs-lookup"><span data-stu-id="ce696-104">Return statement.</span></span>



| <span data-ttu-id="ce696-105">direcc</span><span class="sxs-lookup"><span data-stu-id="ce696-105">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="ce696-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce696-106">Remarks</span></span>

<span data-ttu-id="ce696-107">Si se encuentra dentro de una subrutina, vuelva a la instrucción después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ce696-107">If within a subroutine, return to the instruction after the call.</span></span> <span data-ttu-id="ce696-108">Si no está dentro de una subrutina, finalice la ejecución del programa.</span><span class="sxs-lookup"><span data-stu-id="ce696-108">If not inside a subroutine, terminate program execution.</span></span>

<span data-ttu-id="ce696-109">En el ejemplo siguiente se muestra cómo utilizar esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="ce696-109">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a><span data-ttu-id="ce696-110">Restricciones</span><span class="sxs-lookup"><span data-stu-id="ce696-110">Restrictions</span></span>

-   <span data-ttu-id="ce696-111">**RET** puede aparecer en cualquier parte de un programa, en cualquier número de veces.</span><span class="sxs-lookup"><span data-stu-id="ce696-111">**ret** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="ce696-112">Si aparece una instrucción de [etiqueta](label--sm4---asm-.md) en un sombreador, debe ir precedida de un comando **RET** que no esté anidado en las instrucciones de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="ce696-112">If a [label](label--sm4---asm-.md) instruction appears in a Shader, it must be preceded by a **ret** command that is not nested in any flow control statements.</span></span>
-   <span data-ttu-id="ce696-113">Si hay subrutinas en un sombreador, la última instrucción del sombreador debe ser un **RET**.</span><span class="sxs-lookup"><span data-stu-id="ce696-113">If there are subroutines in a Shader, the last instruction in the Shader must be a **ret**.</span></span>

<span data-ttu-id="ce696-114">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ce696-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ce696-115">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ce696-115">Vertex Shader</span></span> | <span data-ttu-id="ce696-116">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="ce696-116">Geometry Shader</span></span> | <span data-ttu-id="ce696-117">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ce696-117">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ce696-118">x</span><span class="sxs-lookup"><span data-stu-id="ce696-118">x</span></span>             | <span data-ttu-id="ce696-119">x</span><span class="sxs-lookup"><span data-stu-id="ce696-119">x</span></span>               | <span data-ttu-id="ce696-120">x</span><span class="sxs-lookup"><span data-stu-id="ce696-120">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ce696-121">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ce696-121">Minimum Shader Model</span></span>

<span data-ttu-id="ce696-122">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ce696-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ce696-123">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ce696-123">Shader Model</span></span>                                              | <span data-ttu-id="ce696-124">Compatible</span><span class="sxs-lookup"><span data-stu-id="ce696-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ce696-125">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ce696-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ce696-126">sí</span><span class="sxs-lookup"><span data-stu-id="ce696-126">yes</span></span>       |
| [<span data-ttu-id="ce696-127">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ce696-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ce696-128">sí</span><span class="sxs-lookup"><span data-stu-id="ce696-128">yes</span></span>       |
| [<span data-ttu-id="ce696-129">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ce696-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ce696-130">sí</span><span class="sxs-lookup"><span data-stu-id="ce696-130">yes</span></span>       |
| [<span data-ttu-id="ce696-131">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce696-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ce696-132">no</span><span class="sxs-lookup"><span data-stu-id="ce696-132">no</span></span>        |
| [<span data-ttu-id="ce696-133">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce696-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ce696-134">no</span><span class="sxs-lookup"><span data-stu-id="ce696-134">no</span></span>        |
| [<span data-ttu-id="ce696-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce696-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ce696-136">no</span><span class="sxs-lookup"><span data-stu-id="ce696-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ce696-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce696-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce696-138">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce696-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




