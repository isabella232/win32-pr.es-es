---
description: Especifica el nivel de calidad de la codificación.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Propiedad AVEncCommonQuality (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e69d797f2e26e830158c969c8fcf4ec0b242a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495635"
---
# <a name="avenccommonquality-property"></a><span data-ttu-id="40e37-103">Propiedad AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="40e37-103">AVEncCommonQuality property</span></span>

<span data-ttu-id="40e37-104">Especifica el nivel de calidad de la codificación.</span><span class="sxs-lookup"><span data-stu-id="40e37-104">Specifies the quality level for encoding.</span></span>

<span data-ttu-id="40e37-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="40e37-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="40e37-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="40e37-106">Data type</span></span>

<span data-ttu-id="40e37-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="40e37-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="40e37-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="40e37-108">Property GUID</span></span>

<span data-ttu-id="40e37-109">**CODECAPI \_ AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="40e37-109">**CODECAPI\_AVEncCommonQuality**</span></span>

## <a name="property-value"></a><span data-ttu-id="40e37-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="40e37-110">Property value</span></span>

<span data-ttu-id="40e37-111">El valor de esta propiedad tiene el siguiente intervalo.</span><span class="sxs-lookup"><span data-stu-id="40e37-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="40e37-112">Value</span><span class="sxs-lookup"><span data-stu-id="40e37-112">Value</span></span> | <span data-ttu-id="40e37-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="40e37-113">Description</span></span>                           |
|-------|---------------------------------------|
| <span data-ttu-id="40e37-114">0</span><span class="sxs-lookup"><span data-stu-id="40e37-114">0</span></span>     | <span data-ttu-id="40e37-115">Calidad mínima, menor tamaño de salida.</span><span class="sxs-lookup"><span data-stu-id="40e37-115">Minimum quality, smaller output size.</span></span> |
| <span data-ttu-id="40e37-116">100</span><span class="sxs-lookup"><span data-stu-id="40e37-116">100</span></span>   | <span data-ttu-id="40e37-117">Calidad máxima, mayor tamaño de salida.</span><span class="sxs-lookup"><span data-stu-id="40e37-117">Maximum quality, larger output size.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="40e37-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40e37-118">Remarks</span></span>

<span data-ttu-id="40e37-119">Esta propiedad controla el nivel de calidad cuando el codificador no usa una velocidad de bits restringida.</span><span class="sxs-lookup"><span data-stu-id="40e37-119">This property controls the quality level when the encoder is not using a constrained bit rate.</span></span> <span data-ttu-id="40e37-120">La propiedad [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) determina si la velocidad de bits está restringida.</span><span class="sxs-lookup"><span data-stu-id="40e37-120">The [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) property determines whether the bit rate is constrained.</span></span>

## <a name="requirements"></a><span data-ttu-id="40e37-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40e37-121">Requirements</span></span>



| <span data-ttu-id="40e37-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="40e37-122">Requirement</span></span> | <span data-ttu-id="40e37-123">Value</span><span class="sxs-lookup"><span data-stu-id="40e37-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40e37-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40e37-124">Minimum supported client</span></span><br/> | <span data-ttu-id="40e37-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="40e37-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="40e37-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40e37-126">Minimum supported server</span></span><br/> | <span data-ttu-id="40e37-127">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="40e37-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="40e37-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40e37-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="40e37-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="40e37-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40e37-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="40e37-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40e37-131">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="40e37-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="40e37-132">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="40e37-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




