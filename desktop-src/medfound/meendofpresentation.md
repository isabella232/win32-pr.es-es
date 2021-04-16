---
description: Lo genera un origen multimedia cuando finaliza una presentación. Este evento indica que se han completado todas las secuencias de la presentación. La sesión multimedia reenvía este evento a la aplicación.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Evento MEEndOfPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e3a904725908d83afd54bbd64012420075037a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652543"
---
# <a name="meendofpresentation-event"></a><span data-ttu-id="ea4c4-105">Evento MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="ea4c4-105">MEEndOfPresentation event</span></span>

<span data-ttu-id="ea4c4-106">Lo genera un origen multimedia cuando finaliza una presentación.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-106">Raised by a media source when a presentation ends.</span></span> <span data-ttu-id="ea4c4-107">Este evento indica que se han completado todas las secuencias de la presentación.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-107">This event signals that all streams in the presentation are complete.</span></span> <span data-ttu-id="ea4c4-108">La sesión multimedia reenvía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="ea4c4-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="ea4c4-109">Event values</span></span>

<span data-ttu-id="ea4c4-110">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ea4c4-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ea4c4-111">VARTYPE</span></span>              | <span data-ttu-id="ea4c4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea4c4-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ea4c4-113">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="ea4c4-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ea4c4-114">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="ea4c4-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="ea4c4-115">Attributes</span></span>

<span data-ttu-id="ea4c4-116">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="ea4c4-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea4c4-117">Attribute</span></span>                                                                                               | <span data-ttu-id="ea4c4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea4c4-118">Description</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea4c4-119">**\_topología de origen de eventos MF \_ \_ \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="ea4c4-119">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="ea4c4-120">Especifica si el origen del secuenciador canceló esta presentación.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-120">Specifies whether the sequencer source canceled this presentation.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ea4c4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea4c4-121">Requirements</span></span>



| <span data-ttu-id="ea4c4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea4c4-122">Requirement</span></span> | <span data-ttu-id="ea4c4-123">Value</span><span class="sxs-lookup"><span data-stu-id="ea4c4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4c4-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea4c4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4c4-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ea4c4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ea4c4-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea4c4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4c4-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea4c4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ea4c4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea4c4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea4c4-129"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea4c4-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4c4-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea4c4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4c4-131">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea4c4-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




