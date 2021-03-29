---
description: La inicia la sesión de medios cuando cambia el estado de una topología.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Evento MESessionTopologyStatus (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001515"
---
# <a name="mesessiontopologystatus-event"></a><span data-ttu-id="9e3a6-103">Evento MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="9e3a6-103">MESessionTopologyStatus event</span></span>

<span data-ttu-id="9e3a6-104">La inicia la sesión de medios cuando cambia el estado de una topología.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-104">Raised by the Media Session when the status of a topology changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="9e3a6-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="9e3a6-105">Event values</span></span>

<span data-ttu-id="9e3a6-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9e3a6-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9e3a6-107">VARTYPE</span></span>                | <span data-ttu-id="9e3a6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e3a6-108">Description</span></span>                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e3a6-109">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="9e3a6-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="9e3a6-110">Puntero a la interfaz [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topología.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-110">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="9e3a6-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="9e3a6-111">Attributes</span></span>

<span data-ttu-id="9e3a6-112">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="9e3a6-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="9e3a6-113">Attribute</span></span>                                                                            | <span data-ttu-id="9e3a6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e3a6-114">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="9e3a6-115">**Estado de la \_ topología de eventos MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e3a6-115">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)<br/> | <span data-ttu-id="9e3a6-116">Especifica el nuevo estado de la topología.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-116">Specifies the new status of the topology.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9e3a6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e3a6-117">Remarks</span></span>

<span data-ttu-id="9e3a6-118">Para obtener un ejemplo de código que recupera el puntero [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) del evento, vea el evento [MESessionTopologySet](mesessiontopologyset.md) .</span><span class="sxs-lookup"><span data-stu-id="9e3a6-118">For a code example that retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from the event, see [MESessionTopologySet](mesessiontopologyset.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e3a6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e3a6-119">Requirements</span></span>



| <span data-ttu-id="9e3a6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e3a6-120">Requirement</span></span> | <span data-ttu-id="9e3a6-121">Value</span><span class="sxs-lookup"><span data-stu-id="9e3a6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e3a6-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e3a6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9e3a6-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e3a6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9e3a6-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e3a6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9e3a6-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e3a6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9e3a6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e3a6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e3a6-127"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e3a6-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e3a6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e3a6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e3a6-129">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e3a6-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




