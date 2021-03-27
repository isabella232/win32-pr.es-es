---
title: descartar (SM4-ASM)
description: Marca condicionalmente los resultados del sombreador de píxeles que se descartan cuando se alcanza el final del programa.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d98365ae6d80710f15cf7204f98d810be30a13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103994827"
---
# <a name="discard-sm4---asm"></a><span data-ttu-id="8ec01-103">descartar (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8ec01-103">discard (sm4 - asm)</span></span>

<span data-ttu-id="8ec01-104">Marca condicionalmente los resultados del sombreador de píxeles que se descartan cuando se alcanza el final del programa.</span><span class="sxs-lookup"><span data-stu-id="8ec01-104">Conditionally flag results of Pixel Shader to be discarded when the end of the program is reached.</span></span>



| <span data-ttu-id="8ec01-105">descartar { \_ z </span><span class="sxs-lookup"><span data-stu-id="8ec01-105">discard{\_z</span></span>\|<span data-ttu-id="8ec01-106">\_NZ} src0. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="8ec01-106">\_nz} src0.select\_component</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="8ec01-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="8ec01-107">Item</span></span>                                                            | <span data-ttu-id="8ec01-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ec01-108">Description</span></span>                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec01-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8ec01-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="8ec01-110">\[en \] el valor que determina si se va a descartar el píxel actual que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="8ec01-110">\[in\] The value that determines whether to discard the current pixel being processed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8ec01-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ec01-111">Remarks</span></span>

<span data-ttu-id="8ec01-112">Esta instrucción marca el píxel actual como terminado, mientras continúa la ejecución, de modo que otros píxeles que se ejecuten en paralelo puedan obtener derivados si es necesario.</span><span class="sxs-lookup"><span data-stu-id="8ec01-112">This instruction flags the current pixel as terminated, while continuing execution, so that other pixels executing in parallel may obtain derivatives if necessary.</span></span> <span data-ttu-id="8ec01-113">Aunque la ejecución continúa, se descartan todos los resultados del sombreador de píxeles antes o después de la instrucción de **descarte** .</span><span class="sxs-lookup"><span data-stu-id="8ec01-113">Even though execution continues, all Pixel Shader output writes before or after the **discard** instruction are discarded.</span></span>

<span data-ttu-id="8ec01-114">Para **descartar \_ z**, si todos los bits del *\_ componente src0. Select* son cero, se descarta el píxel.</span><span class="sxs-lookup"><span data-stu-id="8ec01-114">For **discard\_z**, if all bits in *src0.select\_component* are zero, then the pixel is discarded.</span></span>

<span data-ttu-id="8ec01-115">Para **descartar \_ NZ**, si algún bit del *\_ componente src0. Select* es distinto de cero, se descarta el píxel.</span><span class="sxs-lookup"><span data-stu-id="8ec01-115">For **discard\_nz**, if any bits in *src0.select\_component* are nonzero, then the pixel is discarded.</span></span>

<span data-ttu-id="8ec01-116">Además, la instrucción **discard** puede estar presente dentro de cualquier construcción de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="8ec01-116">In addition, the **discard** instruction can be present inside any flow control construct.</span></span>

<span data-ttu-id="8ec01-117">Pueden existir varias instrucciones de **descarte** en un sombreador y, si se ejecuta alguna, se termina el píxel.</span><span class="sxs-lookup"><span data-stu-id="8ec01-117">Multiple **discard** instructions may be present in a Shader, and if any is executed, the pixel is terminated.</span></span>

<span data-ttu-id="8ec01-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="8ec01-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8ec01-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="8ec01-119">Vertex Shader</span></span> | <span data-ttu-id="8ec01-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="8ec01-120">Geometry Shader</span></span> | <span data-ttu-id="8ec01-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8ec01-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="8ec01-122">x</span><span class="sxs-lookup"><span data-stu-id="8ec01-122">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8ec01-123">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="8ec01-123">Minimum Shader Model</span></span>

<span data-ttu-id="8ec01-124">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8ec01-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8ec01-125">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="8ec01-125">Shader Model</span></span>                                              | <span data-ttu-id="8ec01-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="8ec01-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8ec01-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8ec01-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8ec01-128">sí</span><span class="sxs-lookup"><span data-stu-id="8ec01-128">yes</span></span>       |
| [<span data-ttu-id="8ec01-129">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8ec01-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8ec01-130">sí</span><span class="sxs-lookup"><span data-stu-id="8ec01-130">yes</span></span>       |
| [<span data-ttu-id="8ec01-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8ec01-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8ec01-132">sí</span><span class="sxs-lookup"><span data-stu-id="8ec01-132">yes</span></span>       |
| [<span data-ttu-id="8ec01-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ec01-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8ec01-134">no</span><span class="sxs-lookup"><span data-stu-id="8ec01-134">no</span></span>        |
| [<span data-ttu-id="8ec01-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ec01-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8ec01-136">no</span><span class="sxs-lookup"><span data-stu-id="8ec01-136">no</span></span>        |
| [<span data-ttu-id="8ec01-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ec01-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8ec01-138">no</span><span class="sxs-lookup"><span data-stu-id="8ec01-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8ec01-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ec01-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ec01-140">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ec01-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





