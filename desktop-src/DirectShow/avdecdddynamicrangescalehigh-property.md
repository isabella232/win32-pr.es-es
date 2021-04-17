---
description: Especifica el corte de alto nivel cuando el descodificador realiza el control de intervalo dinámico en una secuencia de audio Dolby AC-3.
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: Propiedad AVDecDDDynamicRangeScaleHigh (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521cd631d92db73f23c7018adeda9bd321d23c1a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495461"
---
# <a name="avdecdddynamicrangescalehigh-property"></a><span data-ttu-id="37eef-103">Propiedad AVDecDDDynamicRangeScaleHigh</span><span class="sxs-lookup"><span data-stu-id="37eef-103">AVDecDDDynamicRangeScaleHigh property</span></span>

<span data-ttu-id="37eef-104">Especifica el corte de alto nivel cuando el descodificador realiza el control de intervalo dinámico en una secuencia de audio Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="37eef-104">Specifies the high-level cut when the decoder performs dynamic range control on a Dolby AC-3 audio stream.</span></span>

<span data-ttu-id="37eef-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="37eef-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="37eef-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="37eef-106">Data type</span></span>

<span data-ttu-id="37eef-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="37eef-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="37eef-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="37eef-108">Property GUID</span></span>

<span data-ttu-id="37eef-109">**CODECAPI \_ AVDecDDDynamicRangeScaleHigh**</span><span class="sxs-lookup"><span data-stu-id="37eef-109">**CODECAPI\_AVDecDDDynamicRangeScaleHigh**</span></span>

## <a name="property-value"></a><span data-ttu-id="37eef-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="37eef-110">Property value</span></span>

<span data-ttu-id="37eef-111">El valor de esta propiedad tiene el siguiente intervalo.</span><span class="sxs-lookup"><span data-stu-id="37eef-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="37eef-112">Value</span><span class="sxs-lookup"><span data-stu-id="37eef-112">Value</span></span> | <span data-ttu-id="37eef-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="37eef-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="37eef-114">0</span><span class="sxs-lookup"><span data-stu-id="37eef-114">0</span></span>     | <span data-ttu-id="37eef-115">Sin compresión de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="37eef-115">No dynamic range compression.</span></span> <span data-ttu-id="37eef-116">Conserva el intervalo dinámico completo.</span><span class="sxs-lookup"><span data-stu-id="37eef-116">Preserve the full dynamic range.</span></span> |
| <span data-ttu-id="37eef-117">100</span><span class="sxs-lookup"><span data-stu-id="37eef-117">100</span></span>   | <span data-ttu-id="37eef-118">Aplique la compresión de intervalo dinámico completa.</span><span class="sxs-lookup"><span data-stu-id="37eef-118">Apply full dynamic range compression.</span></span>                          |



 

## <a name="remarks"></a><span data-ttu-id="37eef-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37eef-119">Remarks</span></span>

<span data-ttu-id="37eef-120">Esta propiedad solo se aplica cuando el valor de la propiedad [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) es eAVDecDDOperationalMode \_ line.</span><span class="sxs-lookup"><span data-stu-id="37eef-120">This property applies only when the value of the [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) property is eAVDecDDOperationalMode\_LINE.</span></span>

## <a name="requirements"></a><span data-ttu-id="37eef-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37eef-121">Requirements</span></span>



| <span data-ttu-id="37eef-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="37eef-122">Requirement</span></span> | <span data-ttu-id="37eef-123">Value</span><span class="sxs-lookup"><span data-stu-id="37eef-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37eef-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37eef-124">Minimum supported client</span></span><br/> | <span data-ttu-id="37eef-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="37eef-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="37eef-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37eef-126">Minimum supported server</span></span><br/> | <span data-ttu-id="37eef-127">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="37eef-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="37eef-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37eef-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="37eef-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="37eef-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37eef-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="37eef-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37eef-131">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="37eef-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="37eef-132">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="37eef-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




