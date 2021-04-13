---
description: Indica que un origen multimedia ha completado un intento de volver a conectarse al servidor.
ms.assetid: 228e069a-a26b-472e-915e-ff9aec5ee9c1
title: Evento MEReconnectEnd (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3477abd5d4413faa6b2d965f7ace2d19c48dd786
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544382"
---
# <a name="mereconnectend-event"></a><span data-ttu-id="394a0-103">Evento MEReconnectEnd</span><span class="sxs-lookup"><span data-stu-id="394a0-103">MEReconnectEnd event</span></span>

<span data-ttu-id="394a0-104">Indica que un origen multimedia ha completado un intento de volver a conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="394a0-104">Signals that a media source has completed an attempt to reconnect to the server.</span></span>

<span data-ttu-id="394a0-105">Generado por un origen multimedia al final de un intento de reconexión.</span><span class="sxs-lookup"><span data-stu-id="394a0-105">Raised by a media source at the end of a reconnection attempt.</span></span> <span data-ttu-id="394a0-106">El origen de red genera este evento si se vuelve a conectar al servidor.</span><span class="sxs-lookup"><span data-stu-id="394a0-106">The network source raises this event if it reconnects to the server.</span></span> <span data-ttu-id="394a0-107">La sesión multimedia reenvía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="394a0-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="394a0-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="394a0-108">Event values</span></span>

<span data-ttu-id="394a0-109">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="394a0-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="394a0-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="394a0-110">VARTYPE</span></span>              | <span data-ttu-id="394a0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="394a0-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="394a0-112">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="394a0-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="394a0-113">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="394a0-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="394a0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="394a0-114">Requirements</span></span>



| <span data-ttu-id="394a0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="394a0-115">Requirement</span></span> | <span data-ttu-id="394a0-116">Value</span><span class="sxs-lookup"><span data-stu-id="394a0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="394a0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="394a0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="394a0-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="394a0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="394a0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="394a0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="394a0-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="394a0-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="394a0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="394a0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="394a0-122"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="394a0-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="394a0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="394a0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="394a0-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="394a0-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




