---
description: Indica que un origen multimedia está intentando volver a conectarse al servidor.
ms.assetid: c5975279-c710-4046-9152-d1e1c62eb785
title: Evento MEReconnectStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21944e937f52205416b5e6e2b52d18c3a3c768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155588"
---
# <a name="mereconnectstart-event"></a><span data-ttu-id="da543-103">Evento MEReconnectStart</span><span class="sxs-lookup"><span data-stu-id="da543-103">MEReconnectStart event</span></span>

<span data-ttu-id="da543-104">Indica que un origen multimedia está intentando volver a conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="da543-104">Signals that a media source is attempting to reconnect to the server.</span></span>

<span data-ttu-id="da543-105">Generado por un origen multimedia al inicio de un intento de reconexión.</span><span class="sxs-lookup"><span data-stu-id="da543-105">Raised by a media source at the start of a reconnection attempt.</span></span> <span data-ttu-id="da543-106">El origen de red genera este evento si intenta volver a conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="da543-106">The network source raises this event if it attempts to reconnect to the server.</span></span> <span data-ttu-id="da543-107">La sesión multimedia reenvía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da543-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="da543-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="da543-108">Event values</span></span>

<span data-ttu-id="da543-109">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="da543-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="da543-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="da543-110">VARTYPE</span></span>              | <span data-ttu-id="da543-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="da543-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="da543-112">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="da543-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="da543-113">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="da543-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="da543-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da543-114">Requirements</span></span>



| <span data-ttu-id="da543-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="da543-115">Requirement</span></span> | <span data-ttu-id="da543-116">Value</span><span class="sxs-lookup"><span data-stu-id="da543-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da543-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da543-117">Minimum supported client</span></span><br/> | <span data-ttu-id="da543-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="da543-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da543-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da543-119">Minimum supported server</span></span><br/> | <span data-ttu-id="da543-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="da543-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da543-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da543-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="da543-122"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da543-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da543-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="da543-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da543-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da543-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




