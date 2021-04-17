---
description: Indica el número de búferes sin comprimir que requiere el receptor multimedia del representador de vídeo mejorado (EVR) para Desentrelazar.
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: MF_SA_REQUIRED_SAMPLE_COUNT atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716347"
---
# <a name="mf_sa_required_sample_count-attribute"></a><span data-ttu-id="69f84-103">Se \_ \_ requiere el \_ atributo de \_ recuento de muestras de MF SA</span><span class="sxs-lookup"><span data-stu-id="69f84-103">MF\_SA\_REQUIRED\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="69f84-104">Indica el número de búferes sin comprimir que requiere el receptor multimedia del representador de vídeo mejorado (EVR) para Desentrelazar.</span><span class="sxs-lookup"><span data-stu-id="69f84-104">Indicates the number of uncompressed buffers that the enhanced video renderer (EVR) media sink requires for deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="69f84-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="69f84-105">Data type</span></span>

<span data-ttu-id="69f84-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="69f84-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="69f84-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69f84-107">Remarks</span></span>

<span data-ttu-id="69f84-108">Este es un atributo de nivel de secuencia.</span><span class="sxs-lookup"><span data-stu-id="69f84-108">This is a stream-level attribute.</span></span> <span data-ttu-id="69f84-109">Para obtener el atributo de EVR, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="69f84-109">To get the attribute from the EVR, do the following:</span></span>

1.  <span data-ttu-id="69f84-110">Llame a [**IMFMediaSink:: GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) para obtener el receptor de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="69f84-110">Call [**IMFMediaSink::GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) to get the stream sink.</span></span>
2.  <span data-ttu-id="69f84-111">Consulte el receptor de la secuencia para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="69f84-111">Query the stream sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>
3.  <span data-ttu-id="69f84-112">Llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="69f84-112">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="69f84-113">Internamente, el mezclador proporciona este atributo a EVR.</span><span class="sxs-lookup"><span data-stu-id="69f84-113">Internally, the mixer provides this attribute to the EVR.</span></span> <span data-ttu-id="69f84-114">Para obtener el atributo del mezclador, llame a [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="69f84-114">To get the attribute from the mixer, call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span></span>

<span data-ttu-id="69f84-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="69f84-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="69f84-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69f84-116">Requirements</span></span>



| <span data-ttu-id="69f84-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="69f84-117">Requirement</span></span> | <span data-ttu-id="69f84-118">Value</span><span class="sxs-lookup"><span data-stu-id="69f84-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f84-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69f84-119">Minimum supported client</span></span><br/> | <span data-ttu-id="69f84-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="69f84-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="69f84-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69f84-121">Minimum supported server</span></span><br/> | <span data-ttu-id="69f84-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="69f84-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="69f84-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69f84-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="69f84-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="69f84-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69f84-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="69f84-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f84-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69f84-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="69f84-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="69f84-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="69f84-128">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="69f84-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="69f84-129">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69f84-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




