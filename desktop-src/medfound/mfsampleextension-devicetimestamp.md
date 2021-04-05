---
description: Contiene la marca de tiempo del controlador de dispositivo.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: MFSampleExtension_DeviceTimestamp atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b354ecd0e399fc297d3677d29b88847f9eba8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908652"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a><span data-ttu-id="b468c-103">\_Atributo DeviceTimestamp de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="b468c-103">MFSampleExtension\_DeviceTimestamp attribute</span></span>

<span data-ttu-id="b468c-104">Contiene la marca de tiempo del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b468c-104">Contains the time stamp from the device driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="b468c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b468c-105">Data type</span></span>

<span data-ttu-id="b468c-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="b468c-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="b468c-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="b468c-107">Get/set</span></span>

<span data-ttu-id="b468c-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="b468c-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="b468c-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="b468c-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b468c-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="b468c-110">Applies to</span></span>

[<span data-ttu-id="b468c-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="b468c-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="b468c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b468c-112">Remarks</span></span>

<span data-ttu-id="b468c-113">Este atributo se establece en los ejemplos de medios creados por un origen de medios para un dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="b468c-113">This attribute is set on media samples created by a media source for a capture device.</span></span> <span data-ttu-id="b468c-114">El valor de este atributo está en el dominio [**MFTIME**](mftime.md) , compartiendo un período de tiempo con el contador de rendimiento de consultas (QPC) y siempre se expresa en unidades de 100 NS.</span><span class="sxs-lookup"><span data-stu-id="b468c-114">This attribute's value is in the [**MFTIME**](mftime.md) domain, sharing an epoch with query performance counter (QPC) time and always expressed in 100ns units.</span></span> <span data-ttu-id="b468c-115">Este atributo está disponible para MFTs insertado en la canalización de captura.</span><span class="sxs-lookup"><span data-stu-id="b468c-115">This attribute is available for MFTs inserted into the capture pipeline.</span></span>

<span data-ttu-id="b468c-116">Para obtener la marca de tiempo relativa al inicio de la transmisión por secuencias, llame al método [**IMFSample:: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) .</span><span class="sxs-lookup"><span data-stu-id="b468c-116">To get the time stamp relative to the start of streaming, call the [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) method.</span></span>

<span data-ttu-id="b468c-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b468c-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b468c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b468c-118">Requirements</span></span>



| <span data-ttu-id="b468c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b468c-119">Requirement</span></span> | <span data-ttu-id="b468c-120">Value</span><span class="sxs-lookup"><span data-stu-id="b468c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b468c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b468c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b468c-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b468c-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b468c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b468c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b468c-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b468c-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b468c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b468c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b468c-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b468c-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b468c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b468c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b468c-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b468c-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b468c-129">Captura de audio y vídeo en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b468c-129">Audio/Video Capture in Media Foundation</span></span>](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="b468c-130">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b468c-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 




