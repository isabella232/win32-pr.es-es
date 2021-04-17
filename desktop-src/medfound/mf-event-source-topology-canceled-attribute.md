---
description: Especifica si el origen del secuenciador canceló una topología.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: MF_EVENT_SOURCE_TOPOLOGY_CANCELED atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a161aec292d834b0418f59f1c26ea2f11a538e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659989"
---
# <a name="mf_event_source_topology_canceled-attribute"></a><span data-ttu-id="86b9a-103">Atributo MF de \_ topología de origen de eventos \_ \_ \_ cancelada</span><span class="sxs-lookup"><span data-stu-id="86b9a-103">MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED attribute</span></span>

<span data-ttu-id="86b9a-104">Especifica si el [origen del secuenciador](sequencer-source.md) canceló una topología.</span><span class="sxs-lookup"><span data-stu-id="86b9a-104">Specifies whether the [Sequencer Source](sequencer-source.md) canceled a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="86b9a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="86b9a-105">Data type</span></span>

<span data-ttu-id="86b9a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="86b9a-106">**UINT32**</span></span>

<span data-ttu-id="86b9a-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="86b9a-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86b9a-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86b9a-108">Remarks</span></span>

<span data-ttu-id="86b9a-109">Este atributo se utiliza con los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="86b9a-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="86b9a-110">MEEndOfPresentationSegment</span><span class="sxs-lookup"><span data-stu-id="86b9a-110">MEEndOfPresentationSegment</span></span>](meendofpresentationsegment.md)
-   [<span data-ttu-id="86b9a-111">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="86b9a-111">MEEndOfPresentation</span></span>](meendofpresentation.md)

<span data-ttu-id="86b9a-112">Si este atributo está presente y es distinto de cero, significa que el segmento de presentación finalizó porque el origen del secuenciador canceló la topología.</span><span class="sxs-lookup"><span data-stu-id="86b9a-112">If this attribute is present and nonzero, it means that the presentation segment ended because the sequencer source canceled the topology.</span></span> <span data-ttu-id="86b9a-113">De lo contrario, el segmento de presentación finalizó con normalidad.</span><span class="sxs-lookup"><span data-stu-id="86b9a-113">Otherwise, the presentation segment ended normally.</span></span>

<span data-ttu-id="86b9a-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="86b9a-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="86b9a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86b9a-115">Requirements</span></span>



| <span data-ttu-id="86b9a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="86b9a-116">Requirement</span></span> | <span data-ttu-id="86b9a-117">Value</span><span class="sxs-lookup"><span data-stu-id="86b9a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="86b9a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86b9a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="86b9a-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="86b9a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="86b9a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86b9a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="86b9a-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="86b9a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="86b9a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86b9a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="86b9a-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="86b9a-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86b9a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="86b9a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b9a-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86b9a-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="86b9a-126">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="86b9a-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="86b9a-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="86b9a-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="86b9a-128">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="86b9a-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="86b9a-129">Eventos de origen de Sequencer</span><span class="sxs-lookup"><span data-stu-id="86b9a-129">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




