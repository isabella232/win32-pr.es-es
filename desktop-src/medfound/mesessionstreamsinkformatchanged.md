---
description: La inicia la sesión de medios cuando el formato cambia en un receptor de medios.
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: Evento MESessionStreamSinkFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed59b9600cbaf8cb942a42beb6bed46d62fc15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275969"
---
# <a name="mesessionstreamsinkformatchanged-event"></a><span data-ttu-id="f9de7-103">Evento MESessionStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="f9de7-103">MESessionStreamSinkFormatChanged event</span></span>

<span data-ttu-id="f9de7-104">La inicia la sesión de medios cuando el formato cambia en un receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="f9de7-104">Raised by the Media Session when the format changes on a media sink.</span></span>

## <a name="event-values"></a><span data-ttu-id="f9de7-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="f9de7-105">Event values</span></span>

<span data-ttu-id="f9de7-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="f9de7-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f9de7-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f9de7-107">VARTYPE</span></span>              | <span data-ttu-id="f9de7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9de7-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="f9de7-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="f9de7-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f9de7-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="f9de7-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="f9de7-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9de7-111">Attributes</span></span>

<span data-ttu-id="f9de7-112">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="f9de7-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="f9de7-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="f9de7-113">Attribute</span></span>                                                                    | <span data-ttu-id="f9de7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9de7-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9de7-115">**\_nodo de \_ salida de evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="f9de7-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="f9de7-116">Identifica el nodo de topología del receptor de medios cuyo formato ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="f9de7-116">Identifies the topology node for the media sink whose format changed.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="f9de7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9de7-117">Requirements</span></span>



| <span data-ttu-id="f9de7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9de7-118">Requirement</span></span> | <span data-ttu-id="f9de7-119">Value</span><span class="sxs-lookup"><span data-stu-id="f9de7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9de7-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9de7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f9de7-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f9de7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f9de7-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9de7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f9de7-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9de7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f9de7-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9de7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9de7-125"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9de7-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9de7-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9de7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9de7-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f9de7-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




