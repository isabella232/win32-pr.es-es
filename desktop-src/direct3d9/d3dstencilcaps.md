---
description: Marcas de capacidad de estarcido de controlador.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e76c42acfcf8b6515e84679ea2fb540178608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423239"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="a0225-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="a0225-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="a0225-104">Marcas de capacidad de estarcido de controlador.</span><span class="sxs-lookup"><span data-stu-id="a0225-104">Driver stencil capability flags.</span></span>



|                          |             |                                                                                                       |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0225-105">\#define</span><span class="sxs-lookup"><span data-stu-id="a0225-105">\#define</span></span>                 | <span data-ttu-id="a0225-106">Value</span><span class="sxs-lookup"><span data-stu-id="a0225-106">Value</span></span>       | <span data-ttu-id="a0225-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0225-107">Description</span></span>                                                                                           |
| <span data-ttu-id="a0225-108">D3DSTENCILCAPS \_ mantener</span><span class="sxs-lookup"><span data-stu-id="a0225-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="a0225-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="a0225-109">0x00000001L</span></span> | <span data-ttu-id="a0225-110">No actualice la entrada en el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="a0225-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="a0225-111">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a0225-111">This is the default value.</span></span>                             |
| <span data-ttu-id="a0225-112">D3DSTENCILCAPS \_ cero</span><span class="sxs-lookup"><span data-stu-id="a0225-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="a0225-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="a0225-113">0x00000002L</span></span> | <span data-ttu-id="a0225-114">Establezca la entrada de búfer de estarcido en 0.</span><span class="sxs-lookup"><span data-stu-id="a0225-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="a0225-115">D3DSTENCILCAPS \_ reemplazar</span><span class="sxs-lookup"><span data-stu-id="a0225-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="a0225-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="a0225-116">0x00000004L</span></span> | <span data-ttu-id="a0225-117">Reemplace la entrada del búfer de estarcido por el valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="a0225-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="a0225-118">D3DSTENCILCAPS \_ INCRSAT</span><span class="sxs-lookup"><span data-stu-id="a0225-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="a0225-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="a0225-119">0x00000008L</span></span> | <span data-ttu-id="a0225-120">Incremente la entrada del búfer de la galería de símbolos y la fijación al valor máximo.</span><span class="sxs-lookup"><span data-stu-id="a0225-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="a0225-121">D3DSTENCILCAPS \_ DECRSAT</span><span class="sxs-lookup"><span data-stu-id="a0225-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="a0225-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="a0225-122">0x00000010L</span></span> | <span data-ttu-id="a0225-123">Disminuya la entrada del búfer de la galería de símbolos, de la abrazadera a cero.</span><span class="sxs-lookup"><span data-stu-id="a0225-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="a0225-124">\_Invertir D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="a0225-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="a0225-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="a0225-125">0x00000020L</span></span> | <span data-ttu-id="a0225-126">Invierta los bits en la entrada de búfer de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="a0225-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="a0225-127">D3DSTENCILCAPS \_ incr</span><span class="sxs-lookup"><span data-stu-id="a0225-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="a0225-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="a0225-128">0x00000040L</span></span> | <span data-ttu-id="a0225-129">Incremente la entrada del búfer de la galería de símbolos, ajustándola a cero si el nuevo valor supera el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="a0225-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="a0225-130">D3DSTENCILCAPS \_ decr (</span><span class="sxs-lookup"><span data-stu-id="a0225-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="a0225-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="a0225-131">0x00000080L</span></span> | <span data-ttu-id="a0225-132">Disminuye la entrada del búfer de estarcido, ajustándola al valor máximo si el nuevo valor es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="a0225-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="a0225-133">D3DSTENCILCAPS \_ TWOSIDED</span><span class="sxs-lookup"><span data-stu-id="a0225-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="a0225-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="a0225-134">0x00000100L</span></span> | <span data-ttu-id="a0225-135">El dispositivo admite la galería de símbolos de dos caras.</span><span class="sxs-lookup"><span data-stu-id="a0225-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="a0225-136">Las entradas de búfer de estarcido son valores enteros comprendidos entre 0 y 2 ⁿ-1, donde n es la profundidad de bits del búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="a0225-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="a0225-137">El miembro StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="a0225-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="a0225-138">Información constante</span><span class="sxs-lookup"><span data-stu-id="a0225-138">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="a0225-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0225-139">Header</span></span>                   | <span data-ttu-id="a0225-140">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="a0225-140">d3d9caps.h</span></span> |
| <span data-ttu-id="a0225-141">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="a0225-141">Minimum operating system</span></span> | <span data-ttu-id="a0225-142">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a0225-142">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a0225-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0225-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0225-144">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a0225-144">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



