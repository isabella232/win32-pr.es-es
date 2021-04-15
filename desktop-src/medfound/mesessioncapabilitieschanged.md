---
description: Lo genera la sesión multimedia cuando cambian las capacidades de la sesión.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Evento MESessionCapabilitiesChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0612b705571c50a6adcbde4afe93b42a524a950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715661"
---
# <a name="mesessioncapabilitieschanged-event"></a><span data-ttu-id="98ce6-103">Evento MESessionCapabilitiesChanged</span><span class="sxs-lookup"><span data-stu-id="98ce6-103">MESessionCapabilitiesChanged event</span></span>

<span data-ttu-id="98ce6-104">Lo genera la sesión multimedia cuando cambian las capacidades de la sesión.</span><span class="sxs-lookup"><span data-stu-id="98ce6-104">Raised by the Media Session when the session capabilities change.</span></span>

## <a name="event-values"></a><span data-ttu-id="98ce6-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="98ce6-105">Event values</span></span>

<span data-ttu-id="98ce6-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="98ce6-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="98ce6-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="98ce6-107">VARTYPE</span></span>              | <span data-ttu-id="98ce6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="98ce6-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="98ce6-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="98ce6-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="98ce6-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="98ce6-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="98ce6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98ce6-111">Remarks</span></span>

<span data-ttu-id="98ce6-112">El evento contiene los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="98ce6-112">The event contains the following attributes.</span></span>



| <span data-ttu-id="98ce6-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="98ce6-113">Attribute</span></span>                                                                     | <span data-ttu-id="98ce6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="98ce6-114">Description</span></span>                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="98ce6-115">**\_evento MF \_ SESSIONCAPS**</span><span class="sxs-lookup"><span data-stu-id="98ce6-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)              | <span data-ttu-id="98ce6-116">Marcas de nuevas capacidades de sesión.</span><span class="sxs-lookup"><span data-stu-id="98ce6-116">New session capabilities flags.</span></span>                  |
| [<span data-ttu-id="98ce6-117">**\_SESSIONCAPS de evento MF \_ \_ Delta**</span><span class="sxs-lookup"><span data-stu-id="98ce6-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md) | <span data-ttu-id="98ce6-118">Indica qué marcas de capacidades han cambiado.</span><span class="sxs-lookup"><span data-stu-id="98ce6-118">Indicates which capabilities flags have changed.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="98ce6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98ce6-119">Requirements</span></span>



| <span data-ttu-id="98ce6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="98ce6-120">Requirement</span></span> | <span data-ttu-id="98ce6-121">Value</span><span class="sxs-lookup"><span data-stu-id="98ce6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98ce6-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98ce6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="98ce6-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="98ce6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="98ce6-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98ce6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="98ce6-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="98ce6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="98ce6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98ce6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="98ce6-127"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98ce6-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98ce6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="98ce6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ce6-129">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98ce6-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




