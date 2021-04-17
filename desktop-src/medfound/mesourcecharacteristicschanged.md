---
description: Generado por un origen multimedia cuando cambian las características de los orígenes.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Evento MESourceCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659e9eea0352d131aac4959b2952e8426ae408a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715659"
---
# <a name="mesourcecharacteristicschanged-event"></a><span data-ttu-id="10674-103">Evento MESourceCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="10674-103">MESourceCharacteristicsChanged event</span></span>

<span data-ttu-id="10674-104">Generado por un origen multimedia cuando cambian las características del origen.</span><span class="sxs-lookup"><span data-stu-id="10674-104">Raised by a media source when the source's characteristics change.</span></span>

## <a name="event-values"></a><span data-ttu-id="10674-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="10674-105">Event values</span></span>

<span data-ttu-id="10674-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="10674-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="10674-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="10674-107">VARTYPE</span></span>              | <span data-ttu-id="10674-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="10674-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="10674-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="10674-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="10674-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="10674-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="10674-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="10674-111">Attributes</span></span>

<span data-ttu-id="10674-112">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="10674-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="10674-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="10674-113">Attribute</span></span>                                                                                                   | <span data-ttu-id="10674-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="10674-114">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="10674-115">**\_características del \_ origen de eventos MF \_**</span><span class="sxs-lookup"><span data-stu-id="10674-115">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)<br/>          | <span data-ttu-id="10674-116">Nuevas características del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="10674-116">New characteristics of the media source.</span></span><br/> <br/>      |
| [<span data-ttu-id="10674-117">**\_características de origen de eventos MF \_ \_ \_ anteriores**</span><span class="sxs-lookup"><span data-stu-id="10674-117">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)<br/> | <span data-ttu-id="10674-118">Características anteriores del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="10674-118">Previous characteristics of the media source.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="10674-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10674-119">Requirements</span></span>



| <span data-ttu-id="10674-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="10674-120">Requirement</span></span> | <span data-ttu-id="10674-121">Value</span><span class="sxs-lookup"><span data-stu-id="10674-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10674-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10674-122">Minimum supported client</span></span><br/> | <span data-ttu-id="10674-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="10674-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="10674-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10674-124">Minimum supported server</span></span><br/> | <span data-ttu-id="10674-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="10674-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="10674-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10674-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="10674-127"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10674-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10674-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="10674-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10674-129">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="10674-129">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[<span data-ttu-id="10674-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="10674-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




