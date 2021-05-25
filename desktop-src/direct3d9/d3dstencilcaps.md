---
description: Marcas de funcionalidad de galería de símbolos del controlador.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8999d73044a061cb8eea8f5829351c1d04079462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343060"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="98dbb-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="98dbb-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="98dbb-104">Marcas de funcionalidad de galería de símbolos del controlador.</span><span class="sxs-lookup"><span data-stu-id="98dbb-104">Driver stencil capability flags.</span></span>



| <span data-ttu-id="98dbb-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="98dbb-105">\#define</span></span>                 | <span data-ttu-id="98dbb-106">Valor</span><span class="sxs-lookup"><span data-stu-id="98dbb-106">Value</span></span>       | <span data-ttu-id="98dbb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="98dbb-107">Description</span></span>                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98dbb-108">D3DSTENCILCAPS \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="98dbb-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="98dbb-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="98dbb-109">0x00000001L</span></span> | <span data-ttu-id="98dbb-110">No actualice la entrada en el búfer de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="98dbb-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="98dbb-111">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="98dbb-111">This is the default value.</span></span>                             |
| <span data-ttu-id="98dbb-112">D3DSTENCILCAPS \_ ZERO</span><span class="sxs-lookup"><span data-stu-id="98dbb-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="98dbb-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="98dbb-113">0x00000002L</span></span> | <span data-ttu-id="98dbb-114">Establezca la entrada stencil-buffer en 0.</span><span class="sxs-lookup"><span data-stu-id="98dbb-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="98dbb-115">D3DSTENCILCAPS \_ REPLACE</span><span class="sxs-lookup"><span data-stu-id="98dbb-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="98dbb-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="98dbb-116">0x00000004L</span></span> | <span data-ttu-id="98dbb-117">Reemplace la entrada stencil-buffer por el valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="98dbb-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="98dbb-118">D3DSTENCILCAPS \_ INCRSAT</span><span class="sxs-lookup"><span data-stu-id="98dbb-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="98dbb-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="98dbb-119">0x00000008L</span></span> | <span data-ttu-id="98dbb-120">Incremente la entrada stencil-buffer, fijando al valor máximo.</span><span class="sxs-lookup"><span data-stu-id="98dbb-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="98dbb-121">D3DSTENCILCAPS \_ DECRSAT</span><span class="sxs-lookup"><span data-stu-id="98dbb-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="98dbb-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="98dbb-122">0x00000010L</span></span> | <span data-ttu-id="98dbb-123">Decremento de la entrada stencil-buffer, fijando a cero.</span><span class="sxs-lookup"><span data-stu-id="98dbb-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="98dbb-124">D3DSTENCILCAPS \_ INVERT</span><span class="sxs-lookup"><span data-stu-id="98dbb-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="98dbb-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="98dbb-125">0x00000020L</span></span> | <span data-ttu-id="98dbb-126">Invierta los bits de la entrada stencil-buffer.</span><span class="sxs-lookup"><span data-stu-id="98dbb-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="98dbb-127">D3DSTENCILCAPS \_ INCR</span><span class="sxs-lookup"><span data-stu-id="98dbb-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="98dbb-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="98dbb-128">0x00000040L</span></span> | <span data-ttu-id="98dbb-129">Incremente la entrada stencil-buffer y ajuste a cero si el nuevo valor supera el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="98dbb-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="98dbb-130">D3DSTENCILCAPS \_ DECR</span><span class="sxs-lookup"><span data-stu-id="98dbb-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="98dbb-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="98dbb-131">0x00000080L</span></span> | <span data-ttu-id="98dbb-132">Decremento de la entrada stencil-buffer, ajustando al valor máximo si el nuevo valor es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="98dbb-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="98dbb-133">D3DSTENCILCAPS \_ TWOSIDED</span><span class="sxs-lookup"><span data-stu-id="98dbb-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="98dbb-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="98dbb-134">0x00000100L</span></span> | <span data-ttu-id="98dbb-135">El dispositivo admite galería de símbolos de dos lados.</span><span class="sxs-lookup"><span data-stu-id="98dbb-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="98dbb-136">Las entradas de búfer de galería de símbolos son valores enteros comprendidos entre 0 y 2ⁿ - 1, donde n es la profundidad de bits del búfer de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="98dbb-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="98dbb-137">El miembro StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="98dbb-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="98dbb-138">Información constante</span><span class="sxs-lookup"><span data-stu-id="98dbb-138">Constant Information</span></span>



| <span data-ttu-id="98dbb-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="98dbb-139">Requirement</span></span>                         | <span data-ttu-id="98dbb-140">Value</span><span class="sxs-lookup"><span data-stu-id="98dbb-140">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="98dbb-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98dbb-141">Header</span></span>                   | <span data-ttu-id="98dbb-142">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="98dbb-142">d3d9caps.h</span></span> |
| <span data-ttu-id="98dbb-143">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="98dbb-143">Minimum operating system</span></span> | <span data-ttu-id="98dbb-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="98dbb-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="98dbb-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98dbb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98dbb-146">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="98dbb-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



