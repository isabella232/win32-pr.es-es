---
description: Especifica el nivel de combinación, en decibelios (dB), en una secuencia de audio Dolby digital. Esta propiedad se aplica a los codificadores de audio Dolby digital.
ms.assetid: fcb16d02-af4f-4626-99ee-2831172e5280
title: Propiedad AVEncDDProductionMixLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8a1726db6ab4841b4603a61bcfe39504742db42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666135"
---
# <a name="avencddproductionmixlevel-property"></a><span data-ttu-id="575d5-104">Propiedad AVEncDDProductionMixLevel</span><span class="sxs-lookup"><span data-stu-id="575d5-104">AVEncDDProductionMixLevel property</span></span>

<span data-ttu-id="575d5-105">Especifica el nivel de combinación, en decibelios (dB), en una secuencia de audio Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="575d5-105">Specifies the mixing level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="575d5-106">Esta propiedad se aplica a los codificadores de audio Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="575d5-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="575d5-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="575d5-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="575d5-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="575d5-108">Data type</span></span>

<span data-ttu-id="575d5-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="575d5-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="575d5-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="575d5-110">Property GUID</span></span>

<span data-ttu-id="575d5-111">**CODECAPI \_ AVEncDDProductionMixLevel**</span><span class="sxs-lookup"><span data-stu-id="575d5-111">**CODECAPI\_AVEncDDProductionMixLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="575d5-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="575d5-112">Property value</span></span>

<span data-ttu-id="575d5-113">Esta propiedad tiene un intervalo de valores lineal.</span><span class="sxs-lookup"><span data-stu-id="575d5-113">This property has a linear range of values.</span></span> <span data-ttu-id="575d5-114">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="575d5-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="575d5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="575d5-115">Remarks</span></span>

<span data-ttu-id="575d5-116">Si establece esta propiedad, establezca la propiedad [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="575d5-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="575d5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="575d5-117">Requirements</span></span>



| <span data-ttu-id="575d5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="575d5-118">Requirement</span></span> | <span data-ttu-id="575d5-119">Value</span><span class="sxs-lookup"><span data-stu-id="575d5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="575d5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="575d5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="575d5-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="575d5-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="575d5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="575d5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="575d5-123">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="575d5-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="575d5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="575d5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="575d5-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="575d5-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="575d5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="575d5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="575d5-127">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="575d5-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="575d5-128">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="575d5-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




