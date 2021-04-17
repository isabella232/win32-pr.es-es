---
description: Especifica el parámetro de cuantificación (QP) para la codificación de vídeo.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: Propiedad CODECAPI_AVEncVideoEncodeQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705424"
---
# <a name="codecapi_avencvideoencodeqp-property"></a><span data-ttu-id="0b0be-103">\_Propiedad AVEncVideoEncodeQP de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="0b0be-103">CODECAPI\_AVEncVideoEncodeQP property</span></span>

<span data-ttu-id="0b0be-104">Especifica el parámetro de cuantificación (QP) para la codificación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0b0be-104">Specifies the quantization parameter (QP) for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="0b0be-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0b0be-105">Data type</span></span>

<span data-ttu-id="0b0be-106">**ULONGLONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="0b0be-106">**ULONGLONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="0b0be-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="0b0be-107">Property GUID</span></span>

<span data-ttu-id="0b0be-108">**CODECAPI \_ AVEncVideoEncodeQP**</span><span class="sxs-lookup"><span data-stu-id="0b0be-108">**CODECAPI\_AVEncVideoEncodeQP**</span></span>

## <a name="property-value"></a><span data-ttu-id="0b0be-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0b0be-109">Property value</span></span>

<span data-ttu-id="0b0be-110">Un conjunto de campos de 4 16 bits que se usan para especificar el marco QPs en la codificación de QP fija.</span><span class="sxs-lookup"><span data-stu-id="0b0be-110">A set of four 16-bit fields used to specify the frame QPs in fixed-QP encoding.</span></span>

<span data-ttu-id="0b0be-111">Los campos son:</span><span class="sxs-lookup"><span data-stu-id="0b0be-111">The fields are:</span></span>

-   <span data-ttu-id="0b0be-112">Bits 0-15: QP predeterminado</span><span class="sxs-lookup"><span data-stu-id="0b0be-112">Bits 0-15: Default QP</span></span>
-   <span data-ttu-id="0b0be-113">Bits 16-31: QP usado para I fotogramas</span><span class="sxs-lookup"><span data-stu-id="0b0be-113">Bits 16-31: QP used for I frames</span></span>
-   <span data-ttu-id="0b0be-114">Bits 32-47: QP usado para fotogramas P</span><span class="sxs-lookup"><span data-stu-id="0b0be-114">Bits 32-47: QP used for P frames</span></span>
-   <span data-ttu-id="0b0be-115">Bits 48-63: QP usado para los fotogramas B</span><span class="sxs-lookup"><span data-stu-id="0b0be-115">Bits 48-63: QP used for B frames</span></span>

## <a name="remarks"></a><span data-ttu-id="0b0be-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b0be-116">Remarks</span></span>

<span data-ttu-id="0b0be-117">Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="0b0be-117">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="0b0be-118">Para garantizar un uso coherente en los distintos codificadores, debe suponer que los codificadores solo examinarán el QP predeterminado y pueden ignorar los valores de QP para las imágenes I/P/B.</span><span class="sxs-lookup"><span data-stu-id="0b0be-118">To insure consistent usage across different encoders, you should assume encoders will only look at the default QP and can ignore QP values for I/P/B pictures.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b0be-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b0be-119">Requirements</span></span>



| <span data-ttu-id="0b0be-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b0be-120">Requirement</span></span> | <span data-ttu-id="0b0be-121">Value</span><span class="sxs-lookup"><span data-stu-id="0b0be-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0be-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b0be-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0b0be-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="0b0be-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="0b0be-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b0be-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0b0be-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="0b0be-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0b0be-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b0be-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b0be-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b0be-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b0be-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b0be-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b0be-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b0be-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0b0be-130">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="0b0be-130">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

