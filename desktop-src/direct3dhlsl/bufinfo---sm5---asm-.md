---
title: bufinfo (SM5-ASM)
description: Consultar el recuento de elementos en un búfer (pero no en el búfer de constantes).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996905"
---
# <a name="bufinfo-sm5---asm"></a><span data-ttu-id="a28a5-103">bufinfo (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a28a5-103">bufinfo (sm5 - asm)</span></span>

<span data-ttu-id="a28a5-104">Consultar el recuento de elementos en un búfer (pero no en el búfer de constantes).</span><span class="sxs-lookup"><span data-stu-id="a28a5-104">Query the element count on a buffer (but not the constant buffer).</span></span>



| <span data-ttu-id="a28a5-105">bufinfo dest \[ . Mask \] , srcResource</span><span class="sxs-lookup"><span data-stu-id="a28a5-105">bufinfo dest\[.mask\], srcResource</span></span> |
|------------------------------------|



 



| <span data-ttu-id="a28a5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a28a5-106">Item</span></span>                                                                                                               | <span data-ttu-id="a28a5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a28a5-107">Description</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a28a5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a28a5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="a28a5-109">\[en \] la dirección de los resultados.</span><span class="sxs-lookup"><span data-stu-id="a28a5-109">\[in\] The address of the results.</span></span><br/>                                         |
| <span data-ttu-id="a28a5-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="a28a5-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="a28a5-111">\[en \] búfer, que no sea un búfer de constantes, en un SRV (t \# ) o UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="a28a5-111">\[in\] Buffer, other than a constant Buffer, in an SRV (t\#) or UAV (u\#).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a28a5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a28a5-112">Remarks</span></span>

<span data-ttu-id="a28a5-113">Todos los componentes de *dest* reciben el número entero de elementos de la vista de recursos del sombreador del búfer.</span><span class="sxs-lookup"><span data-stu-id="a28a5-113">All components in *dest* receive the integer number of elements in the buffer s shader resource view.</span></span> <span data-ttu-id="a28a5-114">El número de elementos depende de los parámetros de vista, como el formato de memoria.</span><span class="sxs-lookup"><span data-stu-id="a28a5-114">The number of elements depends on the view parameters such as memory format.</span></span>

<span data-ttu-id="a28a5-115">En el caso de un búfer con tipo SRV o UAV, el valor devuelto es el número de elementos de la vista (donde un elemento es una unidad del formato con tipo).</span><span class="sxs-lookup"><span data-stu-id="a28a5-115">For a typed buffer SRV or UAV, the return value is the number of elements in the view (where an element is one unit of the typed format).</span></span>

<span data-ttu-id="a28a5-116">En el caso de un búfer sin formato SRV o UAV, el valor devuelto es el número de bytes de la vista.</span><span class="sxs-lookup"><span data-stu-id="a28a5-116">For a raw buffer SRV or UAV, the return value is the number of bytes in the view.</span></span>

<span data-ttu-id="a28a5-117">Para un búfer estructurado SRV o UAV, el valor devuelto es el número de estructuras de la vista.</span><span class="sxs-lookup"><span data-stu-id="a28a5-117">For a structured buffer SRV or UAV, the return value is the number of structures in the view.</span></span>

<span data-ttu-id="a28a5-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="a28a5-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a28a5-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="a28a5-119">Vertex</span></span> | <span data-ttu-id="a28a5-120">Casco</span><span class="sxs-lookup"><span data-stu-id="a28a5-120">Hull</span></span> | <span data-ttu-id="a28a5-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="a28a5-121">Domain</span></span> | <span data-ttu-id="a28a5-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="a28a5-122">Geometry</span></span> | <span data-ttu-id="a28a5-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="a28a5-123">Pixel</span></span> | <span data-ttu-id="a28a5-124">Compute</span><span class="sxs-lookup"><span data-stu-id="a28a5-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a28a5-125">X</span><span class="sxs-lookup"><span data-stu-id="a28a5-125">X</span></span>      | <span data-ttu-id="a28a5-126">X</span><span class="sxs-lookup"><span data-stu-id="a28a5-126">X</span></span>    | <span data-ttu-id="a28a5-127">X</span><span class="sxs-lookup"><span data-stu-id="a28a5-127">X</span></span>      | <span data-ttu-id="a28a5-128">X</span><span class="sxs-lookup"><span data-stu-id="a28a5-128">X</span></span>        | <span data-ttu-id="a28a5-129">X</span><span class="sxs-lookup"><span data-stu-id="a28a5-129">X</span></span>     | <span data-ttu-id="a28a5-130">X</span><span class="sxs-lookup"><span data-stu-id="a28a5-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a28a5-131">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a28a5-131">Minimum Shader Model</span></span>

<span data-ttu-id="a28a5-132">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a28a5-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a28a5-133">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a28a5-133">Shader Model</span></span>                                              | <span data-ttu-id="a28a5-134">Compatible</span><span class="sxs-lookup"><span data-stu-id="a28a5-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a28a5-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a28a5-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a28a5-136">sí</span><span class="sxs-lookup"><span data-stu-id="a28a5-136">yes</span></span>       |
| [<span data-ttu-id="a28a5-137">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a28a5-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a28a5-138">no</span><span class="sxs-lookup"><span data-stu-id="a28a5-138">no</span></span>        |
| [<span data-ttu-id="a28a5-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a28a5-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a28a5-140">no</span><span class="sxs-lookup"><span data-stu-id="a28a5-140">no</span></span>        |
| [<span data-ttu-id="a28a5-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a28a5-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a28a5-142">no</span><span class="sxs-lookup"><span data-stu-id="a28a5-142">no</span></span>        |
| [<span data-ttu-id="a28a5-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a28a5-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a28a5-144">no</span><span class="sxs-lookup"><span data-stu-id="a28a5-144">no</span></span>        |
| [<span data-ttu-id="a28a5-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a28a5-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a28a5-146">no</span><span class="sxs-lookup"><span data-stu-id="a28a5-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a28a5-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a28a5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a28a5-148">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a28a5-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





