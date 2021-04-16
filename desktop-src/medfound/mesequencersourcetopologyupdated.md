---
description: 'Generado por el origen del secuenciador cuando el método IMFSequencerSource:: UpdateTopology se completa de forma asincrónica.'
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: Evento MESequencerSourceTopologyUpdated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715662"
---
# <a name="mesequencersourcetopologyupdated-event"></a><span data-ttu-id="4eddc-103">Evento MESequencerSourceTopologyUpdated</span><span class="sxs-lookup"><span data-stu-id="4eddc-103">MESequencerSourceTopologyUpdated event</span></span>

<span data-ttu-id="4eddc-104">Generado por el origen del secuenciador cuando el método [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="4eddc-104">Raised by the sequencer source when the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="4eddc-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="4eddc-105">Event values</span></span>

<span data-ttu-id="4eddc-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4eddc-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4eddc-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4eddc-107">VARTYPE</span></span>            | <span data-ttu-id="4eddc-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4eddc-108">Description</span></span>                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eddc-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="4eddc-109">VT\_UI4</span></span><br/> | <span data-ttu-id="4eddc-110">Identificador de elemento del secuenciador de la topología que se está actualizando.</span><span class="sxs-lookup"><span data-stu-id="4eddc-110">Sequencer element identifier of the topology that is being updated.</span></span> <span data-ttu-id="4eddc-111">La aplicación especifica este valor en el parámetro *dwId* del método [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) .</span><span class="sxs-lookup"><span data-stu-id="4eddc-111">The application specifies this value in the *dwId* parameter of the [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4eddc-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4eddc-112">Remarks</span></span>

<span data-ttu-id="4eddc-113">Este evento indica que el origen del secuenciador ha actualizado la topología, pero no significa que la topología esté preparada para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="4eddc-113">This event signals that the sequencer source has updated the topology, but does not mean that the topology is ready for playback.</span></span> <span data-ttu-id="4eddc-114">La aplicación debe esperar el evento [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="4eddc-114">The application should wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eddc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4eddc-115">Requirements</span></span>



| <span data-ttu-id="4eddc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eddc-116">Requirement</span></span> | <span data-ttu-id="4eddc-117">Value</span><span class="sxs-lookup"><span data-stu-id="4eddc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eddc-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4eddc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4eddc-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4eddc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4eddc-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4eddc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4eddc-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4eddc-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4eddc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4eddc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eddc-123"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4eddc-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eddc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="4eddc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eddc-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4eddc-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="4eddc-126">Origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="4eddc-126">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




