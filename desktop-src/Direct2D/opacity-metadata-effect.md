---
title: Efecto de metadatos de opacidad
description: Puede usar este efecto para marcar un área de una imagen de entrada como opaca, por lo que es posible realizar optimizaciones de representación internas en el gráfico.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150875"
---
# <a name="opacity-metadata-effect"></a><span data-ttu-id="7b7d4-103">Efecto de metadatos de opacidad</span><span class="sxs-lookup"><span data-stu-id="7b7d4-103">Opacity metadata effect</span></span>

<span data-ttu-id="7b7d4-104">Puede usar este efecto para marcar un área de una imagen de entrada como opaca, por lo que es posible realizar optimizaciones de representación internas en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="7b7d4-104">You can use this effect to mark an area of an input image as opaque, so internal rendering optimizations to the graph are possible.</span></span>

> [!Note]  
> <span data-ttu-id="7b7d4-105">Este efecto no modifica la propia imagen para que sea opaca.</span><span class="sxs-lookup"><span data-stu-id="7b7d4-105">This effect doesn't modify the image itself to be opaque.</span></span> <span data-ttu-id="7b7d4-106">Modifica los datos asociados a la imagen para que el representador asuma que la región especificada es opaca.</span><span class="sxs-lookup"><span data-stu-id="7b7d4-106">It modifies data associated with the image so the renderer assumes the specified region is opaque.</span></span>

 

<span data-ttu-id="7b7d4-107">El CLSID para este efecto es CLSID \_ D2D1OpacityMetadata.</span><span class="sxs-lookup"><span data-stu-id="7b7d4-107">The CLSID for this effect is CLSID\_D2D1OpacityMetadata.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="7b7d4-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="7b7d4-108">Effect properties</span></span>



| <span data-ttu-id="7b7d4-109">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="7b7d4-109">Display name and index enumeration</span></span>                                                 | <span data-ttu-id="7b7d4-110">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7b7d4-110">Type and default value</span></span>                                                             | <span data-ttu-id="7b7d4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b7d4-111">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b7d4-112">OutputRect</span><span class="sxs-lookup"><span data-stu-id="7b7d4-112">OutputRect</span></span><br/> <span data-ttu-id="7b7d4-113">D2D1 \_ OPACITYMETADATA \_ \_ opaco INPUT \_ \_</span><span class="sxs-lookup"><span data-stu-id="7b7d4-113">D2D1\_OPACITYMETADATA\_PROP\_INPUT\_OPAQUE\_RECT</span></span> <br/> | <span data-ttu-id="7b7d4-114">D2D1 \_ Vector \_ 4F</span><span class="sxs-lookup"><span data-stu-id="7b7d4-114">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="7b7d4-115">(-FLT \_ MAX,-FLT \_ Max, FLT \_ Max, FLT \_ Max)</span><span class="sxs-lookup"><span data-stu-id="7b7d4-115">(-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX)</span></span> <br/> | <span data-ttu-id="7b7d4-116">Parte de la imagen de origen opaca.</span><span class="sxs-lookup"><span data-stu-id="7b7d4-116">The portion of the source image that is opaque.</span></span> <span data-ttu-id="7b7d4-117">El valor predeterminado es toda la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="7b7d4-117">The default is the entire input image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7b7d4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b7d4-118">Requirements</span></span>



| <span data-ttu-id="7b7d4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b7d4-119">Requirement</span></span> | <span data-ttu-id="7b7d4-120">Value</span><span class="sxs-lookup"><span data-stu-id="7b7d4-120">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b7d4-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b7d4-121">Minimum supported client</span></span> | <span data-ttu-id="7b7d4-122">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="7b7d4-122">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7b7d4-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b7d4-123">Minimum supported server</span></span> | <span data-ttu-id="7b7d4-124">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="7b7d4-124">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7b7d4-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b7d4-125">Header</span></span>                   | <span data-ttu-id="7b7d4-126">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="7b7d4-126">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="7b7d4-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b7d4-127">Library</span></span>                  | <span data-ttu-id="7b7d4-128">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="7b7d4-128">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="7b7d4-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7b7d4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b7d4-130">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="7b7d4-130">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

