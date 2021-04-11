---
description: Especifica el equilibrio entre la calidad y la velocidad de codificación. Esta propiedad es válida en todos los modos de control de velocidad.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Propiedad AVEncCommonQualityVsSpeed (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8af65f816bc9be6642e2a23ee4dc05e2e4fa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152577"
---
# <a name="avenccommonqualityvsspeed-property"></a><span data-ttu-id="b9e58-104">Propiedad AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="b9e58-104">AVEncCommonQualityVsSpeed property</span></span>

<span data-ttu-id="b9e58-105">Especifica el equilibrio entre la calidad y la velocidad de codificación.</span><span class="sxs-lookup"><span data-stu-id="b9e58-105">Specifies the tradeoff between encoding quality and speed.</span></span> <span data-ttu-id="b9e58-106">Esta propiedad es válida en todos los modos de control de velocidad.</span><span class="sxs-lookup"><span data-stu-id="b9e58-106">This property is valid in all rate control modes.</span></span>

<span data-ttu-id="b9e58-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b9e58-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b9e58-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b9e58-108">Data type</span></span>

<span data-ttu-id="b9e58-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b9e58-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b9e58-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="b9e58-110">Property GUID</span></span>

<span data-ttu-id="b9e58-111">**CODECAPI \_ AVEncCommonQualityVsSpeed**</span><span class="sxs-lookup"><span data-stu-id="b9e58-111">**CODECAPI\_AVEncCommonQualityVsSpeed**</span></span>

## <a name="property-value"></a><span data-ttu-id="b9e58-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b9e58-112">Property value</span></span>

<span data-ttu-id="b9e58-113">El valor de esta propiedad tiene el siguiente intervalo.</span><span class="sxs-lookup"><span data-stu-id="b9e58-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="b9e58-114">Value</span><span class="sxs-lookup"><span data-stu-id="b9e58-114">Value</span></span> | <span data-ttu-id="b9e58-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9e58-115">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="b9e58-116">0</span><span class="sxs-lookup"><span data-stu-id="b9e58-116">0</span></span>     | <span data-ttu-id="b9e58-117">Codificación más rápida y de menor calidad.</span><span class="sxs-lookup"><span data-stu-id="b9e58-117">Lower quality, faster encoding.</span></span>  |
| <span data-ttu-id="b9e58-118">100</span><span class="sxs-lookup"><span data-stu-id="b9e58-118">100</span></span>   | <span data-ttu-id="b9e58-119">Codificación más lenta y de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="b9e58-119">Higher quality, slower encoding.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b9e58-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9e58-120">Requirements</span></span>



| <span data-ttu-id="b9e58-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9e58-121">Requirement</span></span> | <span data-ttu-id="b9e58-122">Value</span><span class="sxs-lookup"><span data-stu-id="b9e58-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e58-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9e58-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b9e58-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="b9e58-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b9e58-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9e58-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b9e58-126">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="b9e58-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b9e58-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9e58-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9e58-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e58-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9e58-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9e58-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e58-130">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="b9e58-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b9e58-131">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="b9e58-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




