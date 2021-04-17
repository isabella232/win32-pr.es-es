---
description: Especifica el ancho y el alto del vídeo codificado, si se recorta el vídeo.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Propiedad AVEncVideoEncodeDimension (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f63d0a5c0d1c6af7c20620c315ad25c16eac528
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666099"
---
# <a name="avencvideoencodedimension-property"></a><span data-ttu-id="8e367-103">Propiedad AVEncVideoEncodeDimension</span><span class="sxs-lookup"><span data-stu-id="8e367-103">AVEncVideoEncodeDimension property</span></span>

<span data-ttu-id="8e367-104">Especifica el ancho y el alto del vídeo codificado, si se recorta el vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e367-104">Specifies the width and height of the encoded video, if the video is cropped.</span></span>

<span data-ttu-id="8e367-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8e367-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8e367-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8e367-106">Data type</span></span>

<span data-ttu-id="8e367-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="8e367-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8e367-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="8e367-108">Property GUID</span></span>

<span data-ttu-id="8e367-109">**CODECAPI \_ AVEncVideoEncodeDimension**</span><span class="sxs-lookup"><span data-stu-id="8e367-109">**CODECAPI\_AVEncVideoEncodeDimension**</span></span>

## <a name="property-value"></a><span data-ttu-id="8e367-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8e367-110">Property value</span></span>

<span data-ttu-id="8e367-111">Los 16 bits superiores del valor contienen el ancho en píxeles y los 16 bits inferiores contienen el alto en píxeles.</span><span class="sxs-lookup"><span data-stu-id="8e367-111">The upper 16 bits of the value contain the width in pixels, and the lower 16 bits contain the height in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e367-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e367-112">Remarks</span></span>

<span data-ttu-id="8e367-113">Las aplicaciones pueden establecer esta propiedad para recortar el vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8e367-113">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="8e367-114">El tamaño especificado debe ser menor que el tamaño de los fotogramas de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8e367-114">The specified size must be less than the size of the input video frames.</span></span> <span data-ttu-id="8e367-115">Use la propiedad [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) para especificar las esquinas izquierda y superior del rectángulo de recorte.</span><span class="sxs-lookup"><span data-stu-id="8e367-115">Use the [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) property to specify the left and top corners of the clipping rectangle.</span></span>

<span data-ttu-id="8e367-116">Los codificadores pueden devolver esta propiedad como una capacidad.</span><span class="sxs-lookup"><span data-stu-id="8e367-116">Encoders can return this property as a capability.</span></span>

<span data-ttu-id="8e367-117">Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="8e367-117">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="8e367-118">En el caso de los codificadores de cámara UVC 1,5, no se admite [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) .</span><span class="sxs-lookup"><span data-stu-id="8e367-118">For UVC 1.5 camera encoders, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e367-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e367-119">Requirements</span></span>



| <span data-ttu-id="8e367-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e367-120">Requirement</span></span> | <span data-ttu-id="8e367-121">Value</span><span class="sxs-lookup"><span data-stu-id="8e367-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e367-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e367-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e367-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="8e367-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8e367-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e367-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e367-125">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="8e367-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8e367-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e367-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e367-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e367-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e367-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e367-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e367-129">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="8e367-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8e367-130">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8e367-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

