---
description: Tiempo de presentación de un ejemplo que se representó durante la limpieza.
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: MF_EVENT_SCRUBSAMPLE_TIME atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7c4fb1a8015367fa3d48edb066cdb135983926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001506"
---
# <a name="mf_event_scrubsample_time-attribute"></a><span data-ttu-id="3e0ed-103">\_Atributo de \_ hora de SCRUBSAMPLE de evento MF \_</span><span class="sxs-lookup"><span data-stu-id="3e0ed-103">MF\_EVENT\_SCRUBSAMPLE\_TIME attribute</span></span>

<span data-ttu-id="3e0ed-104">Tiempo de presentación de un ejemplo que se representó durante la limpieza.</span><span class="sxs-lookup"><span data-stu-id="3e0ed-104">Presentation time for a sample that was rendered while scrubbing.</span></span>

## <a name="data-type"></a><span data-ttu-id="3e0ed-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3e0ed-105">Data type</span></span>

<span data-ttu-id="3e0ed-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="3e0ed-106">**UINT64**</span></span>

<span data-ttu-id="3e0ed-107">Trata como un valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="3e0ed-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e0ed-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e0ed-108">Remarks</span></span>

<span data-ttu-id="3e0ed-109">Este atributo se usa con el evento [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="3e0ed-109">This attribute is used with the [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) event.</span></span>

<span data-ttu-id="3e0ed-110">Este atributo es un valor con signo, aunque se almacena como **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="3e0ed-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="3e0ed-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3e0ed-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e0ed-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e0ed-112">Requirements</span></span>



| <span data-ttu-id="3e0ed-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e0ed-113">Requirement</span></span> | <span data-ttu-id="3e0ed-114">Value</span><span class="sxs-lookup"><span data-stu-id="3e0ed-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3e0ed-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e0ed-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3e0ed-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3e0ed-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3e0ed-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e0ed-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3e0ed-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e0ed-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3e0ed-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e0ed-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e0ed-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e0ed-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e0ed-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e0ed-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e0ed-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e0ed-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3e0ed-123">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="3e0ed-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="3e0ed-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="3e0ed-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="3e0ed-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="3e0ed-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




