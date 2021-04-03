---
description: Especifica el equilibrio entre las imágenes de movimiento y las imágenes fijas. Esta propiedad solo se aplica al modo de control de velocidad de bits constante (CBR).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Propiedad AVEncVideoCBRMotionTradeoff (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b746559f48858f995cbd87184a2f13ada33db7c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997957"
---
# <a name="avencvideocbrmotiontradeoff-property"></a><span data-ttu-id="359df-104">Propiedad AVEncVideoCBRMotionTradeoff</span><span class="sxs-lookup"><span data-stu-id="359df-104">AVEncVideoCBRMotionTradeoff property</span></span>

<span data-ttu-id="359df-105">Especifica el equilibrio entre las imágenes de movimiento y las imágenes fijas.</span><span class="sxs-lookup"><span data-stu-id="359df-105">Specifies the tradeoff between motion and still images.</span></span> <span data-ttu-id="359df-106">Esta propiedad solo se aplica al modo de control de velocidad de bits constante (CBR).</span><span class="sxs-lookup"><span data-stu-id="359df-106">This property applies only to constant bit rate (CBR) control mode.</span></span>

<span data-ttu-id="359df-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="359df-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="359df-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="359df-108">Data type</span></span>

<span data-ttu-id="359df-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="359df-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="359df-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="359df-110">Property GUID</span></span>

<span data-ttu-id="359df-111">**CODECAPI \_ AVEncVideoCBRMotionTradeoff**</span><span class="sxs-lookup"><span data-stu-id="359df-111">**CODECAPI\_AVEncVideoCBRMotionTradeoff**</span></span>

## <a name="property-value"></a><span data-ttu-id="359df-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="359df-112">Property value</span></span>

<span data-ttu-id="359df-113">El valor de esta propiedad tiene el siguiente intervalo.</span><span class="sxs-lookup"><span data-stu-id="359df-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="359df-114">Value</span><span class="sxs-lookup"><span data-stu-id="359df-114">Value</span></span> | <span data-ttu-id="359df-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="359df-115">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="359df-116">0</span><span class="sxs-lookup"><span data-stu-id="359df-116">0</span></span>     | <span data-ttu-id="359df-117">Optimizar para imágenes fijas</span><span class="sxs-lookup"><span data-stu-id="359df-117">Optimize for still images</span></span> |
| <span data-ttu-id="359df-118">100</span><span class="sxs-lookup"><span data-stu-id="359df-118">100</span></span>   | <span data-ttu-id="359df-119">Optimizar para el movimiento.</span><span class="sxs-lookup"><span data-stu-id="359df-119">Optimize for motion.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="359df-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="359df-120">Requirements</span></span>



| <span data-ttu-id="359df-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="359df-121">Requirement</span></span> | <span data-ttu-id="359df-122">Value</span><span class="sxs-lookup"><span data-stu-id="359df-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="359df-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="359df-123">Minimum supported client</span></span><br/> | <span data-ttu-id="359df-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="359df-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="359df-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="359df-125">Minimum supported server</span></span><br/> | <span data-ttu-id="359df-126">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="359df-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="359df-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="359df-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="359df-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="359df-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="359df-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="359df-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="359df-130">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="359df-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="359df-131">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="359df-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




