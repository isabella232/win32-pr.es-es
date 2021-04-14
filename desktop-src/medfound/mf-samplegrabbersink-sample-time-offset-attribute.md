---
description: Desplazamiento entre la marca de tiempo de cada muestra recibida por el enganche de ejemplo y la hora en que el enganche de ejemplo presenta el ejemplo.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648229"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a><span data-ttu-id="6a11e-103">\_Atributo de \_ desplazamiento de hora de ejemplo MF SAMPLEGRABBERSINK \_ \_</span><span class="sxs-lookup"><span data-stu-id="6a11e-103">MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="6a11e-104">Desplazamiento entre la marca de tiempo de cada muestra recibida por el enganche de ejemplo y la hora en que el enganche de ejemplo presenta el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6a11e-104">Offset between the time stamp on each sample received by the sample grabber, and the time when the sample grabber presents the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="6a11e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6a11e-105">Data type</span></span>

<span data-ttu-id="6a11e-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="6a11e-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="6a11e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a11e-107">Remarks</span></span>

<span data-ttu-id="6a11e-108">Puede establecer este atributo en el objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devuelto por la función [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="6a11e-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object that is returned by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="6a11e-109">Este atributo permite que la función de devolución de llamada del enganche de ejemplo reciba ejemplos anteriores al tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="6a11e-109">This attribute enables the sample grabber's callback function to receive samples earlier than the presentation time.</span></span>

<span data-ttu-id="6a11e-110">Cuando el enganche de ejemplo recibe un nuevo ejemplo, presenta el ejemplo en el tiempo *t* − *offset*, donde *t* es la marca de tiempo de la muestra y *offset* es el valor de este atributo.</span><span class="sxs-lookup"><span data-stu-id="6a11e-110">When the sample grabber receives a new sample, it presents the sample at time *t* − *offset*, where *t* is the time stamp on the sample and *offset* is the value of this attribute.</span></span> <span data-ttu-id="6a11e-111">Si no se establece este atributo, el valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="6a11e-111">If this attribute is not set, the default value is zero.</span></span>

<span data-ttu-id="6a11e-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6a11e-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a11e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a11e-113">Requirements</span></span>



| <span data-ttu-id="6a11e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a11e-114">Requirement</span></span> | <span data-ttu-id="6a11e-115">Value</span><span class="sxs-lookup"><span data-stu-id="6a11e-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a11e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a11e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6a11e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6a11e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6a11e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a11e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6a11e-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a11e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6a11e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a11e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a11e-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a11e-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a11e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a11e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a11e-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a11e-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6a11e-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="6a11e-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="6a11e-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="6a11e-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="6a11e-126">**IMFSampleGrabberSinkCallback**</span><span class="sxs-lookup"><span data-stu-id="6a11e-126">**IMFSampleGrabberSinkCallback**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[<span data-ttu-id="6a11e-127">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a11e-127">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




