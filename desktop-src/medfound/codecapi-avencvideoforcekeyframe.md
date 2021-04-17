---
description: Obliga al codificador a codificar el siguiente fotograma como un fotograma clave.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: Propiedad CODECAPI_AVEncVideoForceKeyFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705423"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a><span data-ttu-id="871c5-103">\_Propiedad AVEncVideoForceKeyFrame de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="871c5-103">CODECAPI\_AVEncVideoForceKeyFrame property</span></span>

<span data-ttu-id="871c5-104">Obliga al codificador a codificar el siguiente fotograma como un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="871c5-104">Forces the encoder to code the next frame as a key frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="871c5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="871c5-105">Data type</span></span>

<span data-ttu-id="871c5-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="871c5-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="871c5-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="871c5-107">Property GUID</span></span>

<span data-ttu-id="871c5-108">**CODECAPI \_ AVEncVideoForceKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="871c5-108">**CODECAPI\_AVEncVideoForceKeyFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="871c5-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="871c5-109">Property value</span></span>

<span data-ttu-id="871c5-110">Si el valor es distinto de cero, el codificador codificará el siguiente fotograma como un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="871c5-110">If the value is nonzero, the encoder will code the next frame as a key frame.</span></span> <span data-ttu-id="871c5-111">Si el valor es cero, el codificador selecciona si se debe codificar el fotograma siguiente como un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="871c5-111">If the value is zero, the encoder selects whether to encode the next frame as a key frame.</span></span>

<span data-ttu-id="871c5-112">Esta propiedad se aplica al siguiente fotograma que el codificador recibe como entrada.</span><span class="sxs-lookup"><span data-stu-id="871c5-112">This property applies to the next frame that the encoder receives as input.</span></span> <span data-ttu-id="871c5-113">En el caso de una transformación de Media Foundation (MFT), este es el siguiente fotograma que se pasa al método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) .</span><span class="sxs-lookup"><span data-stu-id="871c5-113">For a Media Foundation transform (MFT), this is the next frame that is passed to the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method.</span></span> <span data-ttu-id="871c5-114">La configuración se restablece en cero después del fotograma siguiente.</span><span class="sxs-lookup"><span data-stu-id="871c5-114">The setting resets to zero after the next frame.</span></span>

## <a name="remarks"></a><span data-ttu-id="871c5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="871c5-115">Remarks</span></span>

<span data-ttu-id="871c5-116">Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="871c5-116">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="871c5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="871c5-117">Requirements</span></span>



| <span data-ttu-id="871c5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="871c5-118">Requirement</span></span> | <span data-ttu-id="871c5-119">Value</span><span class="sxs-lookup"><span data-stu-id="871c5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="871c5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="871c5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="871c5-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="871c5-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="871c5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="871c5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="871c5-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="871c5-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="871c5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="871c5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="871c5-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="871c5-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="871c5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="871c5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="871c5-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="871c5-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="871c5-128">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="871c5-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

