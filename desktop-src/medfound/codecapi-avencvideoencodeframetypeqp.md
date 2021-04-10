---
description: Especifica los tipos de fotogramas (I, P o B) a los que se aplica el parámetro de cuantificación (QP).
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: Propiedad CODECAPI_AVEncVideoEncodeFrameTypeQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153675"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a><span data-ttu-id="19194-103">\_Propiedad AVEncVideoEncodeFrameTypeQP de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="19194-103">CODECAPI\_AVEncVideoEncodeFrameTypeQP property</span></span>

<span data-ttu-id="19194-104">Especifica los tipos de fotogramas (I, P o B) a los que se aplica el parámetro de cuantificación (QP).</span><span class="sxs-lookup"><span data-stu-id="19194-104">Specifies the frame types (I, P, or B) that the quantization parameter (QP) is applied to.</span></span>

## <a name="data-type"></a><span data-ttu-id="19194-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="19194-105">Data type</span></span>

<span data-ttu-id="19194-106">**ULONGULONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="19194-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="19194-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="19194-107">Property GUID</span></span>

<span data-ttu-id="19194-108">**CODECAPI \_ AVEncVideoEncodeFrameTypeQP**</span><span class="sxs-lookup"><span data-stu-id="19194-108">**CODECAPI\_AVEncVideoEncodeFrameTypeQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="19194-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19194-109">Remarks</span></span>

<span data-ttu-id="19194-110">En el caso de los codificadores que admiten la configuración de un parámetro de cuantificación (QP) para diferentes tipos de fotogramas (I, P, B), expondrán esta API además de [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md).</span><span class="sxs-lookup"><span data-stu-id="19194-110">For encoders which support setting a quantization parameter (QP) for different frame types (I, P, B), they shall expose this API in addition to [CODECAPI\_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md).</span></span> <span data-ttu-id="19194-111">Si un codificador solo admite un único QP para todos los tipos de fotogramas, solo admitirá CODECAPI \_ AVEncVideoEncodeQP.</span><span class="sxs-lookup"><span data-stu-id="19194-111">If an encoder supports only a single QP for all frame types, they shall support only CODECAPI\_AVEncVideoEncodeQP.</span></span>

<span data-ttu-id="19194-112">Se trata de una propiedad de codificación dinámica que significa que se puede establecer un nuevo valor en cualquier momento durante la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="19194-112">This is a dynamic encoding property meaning that a new value can be set any time during the encoding session.</span></span>

<span data-ttu-id="19194-113">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="19194-113">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="19194-114">El codificador debe admitir [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="19194-114">Encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="19194-115">Se utiliza un conjunto de campos de 4 16 bits para especificar el marco QPs en la codificación de QP fija.</span><span class="sxs-lookup"><span data-stu-id="19194-115">A set of four 16-bit fields are used to specify the frame QPs in fixed-QP encoding.</span></span> <span data-ttu-id="19194-116">Los campos son:</span><span class="sxs-lookup"><span data-stu-id="19194-116">The fields are:</span></span>

-   <span data-ttu-id="19194-117">**Bits 0-15:** QP usado para I-frames, intervalo válido de \[ 0 a 51 \] .</span><span class="sxs-lookup"><span data-stu-id="19194-117">**Bits 0-15:** QP used for I frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="19194-118">**Bits 16-31:** QP usado para los fotogramas P, intervalo válido de \[ 0 a 51 \] .</span><span class="sxs-lookup"><span data-stu-id="19194-118">**Bits 16-31:** QP used for P frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="19194-119">**Bits 32-47:** QP usado para los fotogramas B, intervalo válido de \[ 0 a 51\]</span><span class="sxs-lookup"><span data-stu-id="19194-119">**Bits 32-47:** QP used for B frames, valid range \[0, 51\]</span></span>
-   <span data-ttu-id="19194-120">**Bits 48-63:** reservado</span><span class="sxs-lookup"><span data-stu-id="19194-120">**Bits 48-63:** reserved</span></span>

<span data-ttu-id="19194-121">Cuando se admite este CodecAPI, los codificadores deben admitir la configuración de QP en el tipo de fotograma I, P y B.</span><span class="sxs-lookup"><span data-stu-id="19194-121">When this CodecAPI is supported, encoders shall support QP setting on frame type of I, P, and B.</span></span>

<span data-ttu-id="19194-122">El valor predeterminado debe ser 0x0000001a001a001a.</span><span class="sxs-lookup"><span data-stu-id="19194-122">Default value shall be 0x0000001a001a001a.</span></span> <span data-ttu-id="19194-123">QP igual a 26 para I, P y B.</span><span class="sxs-lookup"><span data-stu-id="19194-123">QP equal to 26 for I, P and B.</span></span>

<span data-ttu-id="19194-124">Cuando [CODECAPI \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) selecciona una capa temporal específica, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) de CODECAPI \_ AVEncVideoEncodeFrameTypeQP establecerá QP para los fotogramas I, P y B en esa capa temporal.</span><span class="sxs-lookup"><span data-stu-id="19194-124">When [CODECAPI\_AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) selects a specific temporal layer, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) of CODECAPI\_AVEncVideoEncodeFrameTypeQP shall set QP for I, P, and B frames on that temporal layer.</span></span> <span data-ttu-id="19194-125">De forma predeterminada, establece QP para los fotogramas I, P y B en el nivel temporal de la capa temporal base 0.</span><span class="sxs-lookup"><span data-stu-id="19194-125">By default, it sets QP for I, P, and B frames on base temporal layer temporal layer 0.</span></span>

<span data-ttu-id="19194-126">[CODECAPI \_ AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) y [CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md) se usarán para definir y limitar el intervalo de QP para QPs de todos los tipos de imagen, I, P y B.</span><span class="sxs-lookup"><span data-stu-id="19194-126">[CODECAPI\_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) and [CODECAPI\_AVEncVideoMinQP](codecapi-avencvideominqp.md) shall be used to define and limit the QP range for QPs of all picture types, I, P and B.</span></span>

## <a name="requirements"></a><span data-ttu-id="19194-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19194-127">Requirements</span></span>



| <span data-ttu-id="19194-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="19194-128">Requirement</span></span> | <span data-ttu-id="19194-129">Value</span><span class="sxs-lookup"><span data-stu-id="19194-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19194-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19194-130">Minimum supported client</span></span><br/> | <span data-ttu-id="19194-131">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="19194-131">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="19194-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19194-132">Minimum supported server</span></span><br/> | <span data-ttu-id="19194-133">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="19194-133">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="19194-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19194-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="19194-135"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="19194-135"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19194-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="19194-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19194-137">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19194-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

