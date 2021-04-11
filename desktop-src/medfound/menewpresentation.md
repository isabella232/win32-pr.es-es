---
description: Generado por un origen multimedia que proporciona topologías a través de la interfaz IMFMediaSourceTopologyProvider, como el origen del secuenciador. El origen provoca el evento cuando tiene una presentación nueva. La sesión multimedia reenvía este evento a la aplicación.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Evento MENewPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70265a84cc7724fc6f5b6a77be2181149bd82176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275974"
---
# <a name="menewpresentation-event"></a><span data-ttu-id="0d872-105">Evento MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="0d872-105">MENewPresentation event</span></span>

<span data-ttu-id="0d872-106">Generado por un origen multimedia que proporciona topologías a través de la interfaz [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) , como el origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="0d872-106">Raised by a media source that provides topologies through the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface, such as the sequencer source.</span></span> <span data-ttu-id="0d872-107">El origen provoca el evento cuando tiene una presentación nueva.</span><span class="sxs-lookup"><span data-stu-id="0d872-107">The source raises the event when it has a new presentation.</span></span> <span data-ttu-id="0d872-108">La sesión multimedia reenvía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0d872-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="0d872-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="0d872-109">Event values</span></span>

<span data-ttu-id="0d872-110">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="0d872-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0d872-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0d872-111">VARTYPE</span></span>                | <span data-ttu-id="0d872-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d872-112">Description</span></span>                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d872-113">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="0d872-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="0d872-114">Puntero a la interfaz [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descriptor de presentación de la nueva presentación.</span><span class="sxs-lookup"><span data-stu-id="0d872-114">Pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor for the new presentation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0d872-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d872-115">Remarks</span></span>

<span data-ttu-id="0d872-116">La aplicación puede obtener la topología que corresponde al descriptor de presentación mediante una llamada a [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) en el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="0d872-116">The application can get the topology that corresponds to the presentation descriptor by calling [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the media source.</span></span> <span data-ttu-id="0d872-117">A continuación, la aplicación puede poner en cola la nueva topología en la sesión multimedia mediante una llamada a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="0d872-117">The application can then queue the new topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d872-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d872-118">Requirements</span></span>



| <span data-ttu-id="0d872-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d872-119">Requirement</span></span> | <span data-ttu-id="0d872-120">Value</span><span class="sxs-lookup"><span data-stu-id="0d872-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d872-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d872-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d872-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0d872-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0d872-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d872-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d872-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d872-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0d872-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d872-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d872-126"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d872-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d872-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d872-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d872-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0d872-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="0d872-129">Origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="0d872-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




