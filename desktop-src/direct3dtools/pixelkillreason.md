---
description: Enumeración que se usa para indicar por qué se rechazó un píxel.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración PIXELKILLREASON
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359963"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span data-ttu-id="fc913-103"><span id="vspixengine.pixelkillreason"></span>Enumeración PIXELKILLREASON</span><span class="sxs-lookup"><span data-stu-id="fc913-103"><span id="vspixengine.pixelkillreason"></span>PIXELKILLREASON enumeration</span></span>

<span data-ttu-id="fc913-104">Enumeración que se usa para indicar por qué se rechazó un píxel.</span><span class="sxs-lookup"><span data-stu-id="fc913-104">An enum used to indicate why a pixel was rejected.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc913-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc913-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="fc913-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="fc913-106">Constants</span></span>

<span data-ttu-id="fc913-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="fc913-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR\_NONE**</span></span>  
<span data-ttu-id="fc913-108">Valor que indica que no se rechazó el píxel.</span><span class="sxs-lookup"><span data-stu-id="fc913-108">A value that indicates that the pixel was not rejected.</span></span>

<span data-ttu-id="fc913-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**</span><span class="sxs-lookup"><span data-stu-id="fc913-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR\_SHADERKILL**</span></span>  
<span data-ttu-id="fc913-110">Valor que indica que se rechazó el píxel porque no se ejecutó el sombreador.</span><span class="sxs-lookup"><span data-stu-id="fc913-110">A value that indicates that the pixel was rejected because the shader didn't run.</span></span>

<span data-ttu-id="fc913-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ SCISSORTEST**</span><span class="sxs-lookup"><span data-stu-id="fc913-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR\_SCISSORTEST**</span></span>  
<span data-ttu-id="fc913-112">Valor que indica que se rechazó el píxel porque se produjo un error en la prueba de tijera.</span><span class="sxs-lookup"><span data-stu-id="fc913-112">A value that indicates that the pixel was rejected because the scissor test failed.</span></span>

<span data-ttu-id="fc913-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**</span><span class="sxs-lookup"><span data-stu-id="fc913-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR\_ALPHATEST**</span></span>  
<span data-ttu-id="fc913-114">Valor que indica que se rechazó el píxel porque se produjo un error en la prueba alfa.</span><span class="sxs-lookup"><span data-stu-id="fc913-114">A value that indicates that the pixel was rejected because the alpha test failed.</span></span>

<span data-ttu-id="fc913-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="fc913-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR\_STENCILTEST**</span></span>  
<span data-ttu-id="fc913-116">Valor que indica que se rechazó el píxel porque se produjo un error en la prueba de estarcido.</span><span class="sxs-lookup"><span data-stu-id="fc913-116">A value that indicates that the pixel was rejected because the stencil test failed.</span></span>

<span data-ttu-id="fc913-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR \_ DEPTHTEST**</span><span class="sxs-lookup"><span data-stu-id="fc913-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR\_DEPTHTEST**</span></span>  
<span data-ttu-id="fc913-118">Valor que indica que se rechazó el píxel porque se produjo un error en la prueba de profundidad.</span><span class="sxs-lookup"><span data-stu-id="fc913-118">A value that indicates that the pixel was rejected because the depth test failed.</span></span>

<span data-ttu-id="fc913-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**</span><span class="sxs-lookup"><span data-stu-id="fc913-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR\_NOTCOMPUTABLE**</span></span>  
<span data-ttu-id="fc913-120">Valor que indica que no se puede calcular el historial de píxeles.</span><span class="sxs-lookup"><span data-stu-id="fc913-120">A value that indicates that the pixel history can't be computed.</span></span>

<span data-ttu-id="fc913-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**\_error PKR**</span><span class="sxs-lookup"><span data-stu-id="fc913-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR\_ERROR**</span></span>  
<span data-ttu-id="fc913-122">Valor que indica que el píxel se rechazó debido a un error general.</span><span class="sxs-lookup"><span data-stu-id="fc913-122">A value that indicates that the pixel was rejected because of a general error.</span></span>

<span data-ttu-id="fc913-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR \_ Intersection**</span><span class="sxs-lookup"><span data-stu-id="fc913-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR\_NOINTERSECTION**</span></span>  
<span data-ttu-id="fc913-124">Valor que indica que se rechazó el píxel porque la llamada a Draw no forma una intersección con el píxel.</span><span class="sxs-lookup"><span data-stu-id="fc913-124">A value that indicates that the pixel was rejected because the draw call does not intersect the pixel.</span></span>

<span data-ttu-id="fc913-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ ocluidos**</span><span class="sxs-lookup"><span data-stu-id="fc913-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR\_OCCLUDED**</span></span>  
<span data-ttu-id="fc913-126">Valor que indica que se rechazó el píxel porque se ocluidos el dibujo.</span><span class="sxs-lookup"><span data-stu-id="fc913-126">A value that indicates that the pixel was rejected because the draw was occluded.</span></span>

<span data-ttu-id="fc913-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ DEPTHSTENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="fc913-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR\_DEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="fc913-128">Valor que indica que se rechazó el píxel porque no se pudo realizar la prueba de profundidad y de estarcido.</span><span class="sxs-lookup"><span data-stu-id="fc913-128">A value that indicates that the pixel was rejected because the depth and stencil test failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc913-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc913-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fc913-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc913-130">Header</span></span></p></td><td><span data-ttu-id="fc913-131">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fc913-131">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



