---
description: Una enumeración que contiene marcas que se usan para describir un resultado del historial de píxeles. Vea PixelHistoryOperation.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración PIXELHISTORYFLAGS
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152215"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span data-ttu-id="6e133-104"><span id="vspixengine.pixelhistoryflags"></span>Enumeración PIXELHISTORYFLAGS</span><span class="sxs-lookup"><span data-stu-id="6e133-104"><span id="vspixengine.pixelhistoryflags"></span>PIXELHISTORYFLAGS enumeration</span></span>

<span data-ttu-id="6e133-105">Una enumeración que contiene marcas que se usan para describir un resultado del historial de píxeles.</span><span class="sxs-lookup"><span data-stu-id="6e133-105">An enum containing flags used to describe a pixel history result.</span></span> <span data-ttu-id="6e133-106">Vea PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="6e133-106">See PixelHistoryOperation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e133-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e133-107">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="6e133-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="6e133-108">Constants</span></span>

<span data-ttu-id="6e133-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF \_ INITIALVALUE**</span><span class="sxs-lookup"><span data-stu-id="6e133-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF\_INITIALVALUE**</span></span>  
<span data-ttu-id="6e133-110">Marca que corresponde al valor de color inicial (antes del marco).</span><span class="sxs-lookup"><span data-stu-id="6e133-110">A flag that corresponds to the initial color value (prior to frame).</span></span>

<span data-ttu-id="6e133-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ borrar**</span><span class="sxs-lookup"><span data-stu-id="6e133-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF\_CLEAR**</span></span>  
<span data-ttu-id="6e133-112">Marca que corresponde al resultado de color no cifrado.</span><span class="sxs-lookup"><span data-stu-id="6e133-112">A flag that corresponds to the clear color result.</span></span>

<span data-ttu-id="6e133-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF \_ Draw**</span><span class="sxs-lookup"><span data-stu-id="6e133-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF\_DRAW**</span></span>  
<span data-ttu-id="6e133-114">Marca que corresponde al resultado del color de dibujo.</span><span class="sxs-lookup"><span data-stu-id="6e133-114">A flag that corresponds to the draw color result.</span></span>

<span data-ttu-id="6e133-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF \_ FINALVALUE**</span><span class="sxs-lookup"><span data-stu-id="6e133-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF\_FINALVALUE**</span></span>  
<span data-ttu-id="6e133-116">Marca que corresponde al resultado final del color.</span><span class="sxs-lookup"><span data-stu-id="6e133-116">A flag that corresponds to the final color result.</span></span>

<span data-ttu-id="6e133-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF \_ HASCOLOR**</span><span class="sxs-lookup"><span data-stu-id="6e133-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF\_HASCOLOR**</span></span>  
<span data-ttu-id="6e133-118">Marca que corresponde a si el resultado del color está presente en el struct PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="6e133-118">A flag that corresponds to whether the color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="6e133-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF \_ HASFBCOLOR**</span><span class="sxs-lookup"><span data-stu-id="6e133-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF\_HASFBCOLOR**</span></span>  
<span data-ttu-id="6e133-120">Marca que corresponde a si el resultado del color final del búfer está presente en el struct PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="6e133-120">A flag that corresponds to whether the final buffer color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="6e133-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**\_error PHF**</span><span class="sxs-lookup"><span data-stu-id="6e133-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**PHF\_ERROR**</span></span>  

<span data-ttu-id="6e133-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF \_ VERTEXPROCESSINGSKIPPED**</span><span class="sxs-lookup"><span data-stu-id="6e133-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF\_VERTEXPROCESSINGSKIPPED**</span></span>  
<span data-ttu-id="6e133-123">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6e133-123">Not used.</span></span>

<span data-ttu-id="6e133-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF \_ MODIFYRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="6e133-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF\_MODIFYRESOURCE**</span></span>  

<span data-ttu-id="6e133-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF \_ CANNOTRUNFULLDEPTHSTENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="6e133-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF\_CANNOTRUNFULLDEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="6e133-126">Marca que corresponde a no poder ejecutar la prueba de profundidad o de estarcido.</span><span class="sxs-lookup"><span data-stu-id="6e133-126">A flag that corresponds to not being able to run the depth or stencil test.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e133-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e133-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6e133-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e133-128">Header</span></span></p></td><td><span data-ttu-id="6e133-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6e133-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



