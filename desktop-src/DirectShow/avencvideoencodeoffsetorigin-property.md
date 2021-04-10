---
description: Especifica las esquinas izquierda y superior del rectángulo de recorte, si el vídeo se recorta.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Propiedad AVEncVideoEncodeOffsetOrigin (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152238"
---
# <a name="avencvideoencodeoffsetorigin-property"></a><span data-ttu-id="91bb0-103">Propiedad AVEncVideoEncodeOffsetOrigin</span><span class="sxs-lookup"><span data-stu-id="91bb0-103">AVEncVideoEncodeOffsetOrigin property</span></span>

<span data-ttu-id="91bb0-104">Especifica las esquinas izquierda y superior del rectángulo de recorte, si el vídeo se recorta.</span><span class="sxs-lookup"><span data-stu-id="91bb0-104">Specifies the left and top corners of the clipping rectangle, if the video is cropped.</span></span>

<span data-ttu-id="91bb0-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="91bb0-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="91bb0-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="91bb0-106">Data type</span></span>

<span data-ttu-id="91bb0-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="91bb0-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="91bb0-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="91bb0-108">Property GUID</span></span>

<span data-ttu-id="91bb0-109">**CODECAPI \_ AVEncVideoEncodeOffsetOrigin**</span><span class="sxs-lookup"><span data-stu-id="91bb0-109">**CODECAPI\_AVEncVideoEncodeOffsetOrigin**</span></span>

## <a name="property-value"></a><span data-ttu-id="91bb0-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="91bb0-110">Property value</span></span>

<span data-ttu-id="91bb0-111">Los 16 bits superiores del valor contienen el desplazamiento desde el borde izquierdo del fotograma de entrada, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="91bb0-111">The upper 16 bits of the value contain the offset from the left edge of the input frame, in pixels.</span></span> <span data-ttu-id="91bb0-112">Los 16 bits inferiores contienen el desplazamiento desde el borde superior del fotograma de entrada, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="91bb0-112">The lower 16 bits contain the offset from the top edge of the input frame, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="91bb0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91bb0-113">Remarks</span></span>

<span data-ttu-id="91bb0-114">Las aplicaciones pueden establecer esta propiedad para recortar el vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="91bb0-114">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="91bb0-115">Use la propiedad [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) para especificar el ancho y el alto del rectángulo de recorte.</span><span class="sxs-lookup"><span data-stu-id="91bb0-115">Use the [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) property to specify the width and height of the clipping rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="91bb0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91bb0-116">Requirements</span></span>



| <span data-ttu-id="91bb0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="91bb0-117">Requirement</span></span> | <span data-ttu-id="91bb0-118">Value</span><span class="sxs-lookup"><span data-stu-id="91bb0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91bb0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91bb0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="91bb0-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="91bb0-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="91bb0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91bb0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="91bb0-122">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="91bb0-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="91bb0-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91bb0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="91bb0-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="91bb0-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91bb0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="91bb0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91bb0-126">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="91bb0-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="91bb0-127">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="91bb0-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




