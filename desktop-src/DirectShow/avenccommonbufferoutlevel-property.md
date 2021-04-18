---
description: Especifica el nivel final del búfer de codificación, en bits, al final del proceso de codificación. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: Propiedad AVEncCommonBufferOutLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d99cdea909a1fd1c3777aac4868a570161c3fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666140"
---
# <a name="avenccommonbufferoutlevel-property"></a><span data-ttu-id="a75a0-104">Propiedad AVEncCommonBufferOutLevel</span><span class="sxs-lookup"><span data-stu-id="a75a0-104">AVEncCommonBufferOutLevel property</span></span>

<span data-ttu-id="a75a0-105">Especifica el nivel final del búfer de codificación, en bits, al final del proceso de codificación.</span><span class="sxs-lookup"><span data-stu-id="a75a0-105">Specifies the final level of the encoding buffer, in bits, at the end of the encoding process.</span></span> <span data-ttu-id="a75a0-106">Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="a75a0-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="a75a0-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a75a0-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a75a0-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a75a0-108">Data type</span></span>

<span data-ttu-id="a75a0-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a75a0-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a75a0-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="a75a0-110">Property GUID</span></span>

<span data-ttu-id="a75a0-111">**CODECAPI \_ AVEncCommonBufferOutLevel**</span><span class="sxs-lookup"><span data-stu-id="a75a0-111">**CODECAPI\_AVEncCommonBufferOutLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="a75a0-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a75a0-112">Property value</span></span>

<span data-ttu-id="a75a0-113">Esta propiedad tiene un intervalo de valores lineal.</span><span class="sxs-lookup"><span data-stu-id="a75a0-113">This property has a linear range of values.</span></span> <span data-ttu-id="a75a0-114">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="a75a0-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="a75a0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a75a0-115">Remarks</span></span>

<span data-ttu-id="a75a0-116">La propiedad solo está disponible si la duración de la codificación se define de antemano mediante la propiedad [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) o la propiedad [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="a75a0-116">The property is available only if the encoding duration is defined in advance, using the [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) property or [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) property.</span></span>

<span data-ttu-id="a75a0-117">En el vídeo MPEG, esta propiedad define el llenado del comprobador de búfer de vídeo (VBV) al final del proceso de codificación.</span><span class="sxs-lookup"><span data-stu-id="a75a0-117">For MPEG video, this property defines the video buffer verifier (VBV) fullness at the end of the encoding process.</span></span> <span data-ttu-id="a75a0-118">Admite la concatenación de flujos durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="a75a0-118">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75a0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a75a0-119">Requirements</span></span>



| <span data-ttu-id="a75a0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a75a0-120">Requirement</span></span> | <span data-ttu-id="a75a0-121">Value</span><span class="sxs-lookup"><span data-stu-id="a75a0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a75a0-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a75a0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a75a0-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="a75a0-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a75a0-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a75a0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a75a0-125">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="a75a0-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a75a0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a75a0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a75a0-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a75a0-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a75a0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a75a0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a75a0-129">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="a75a0-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a75a0-130">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a75a0-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




