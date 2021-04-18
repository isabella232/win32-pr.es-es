---
description: Generados por los receptores de flujo del representador de vídeo mejorado (EVR) si cambia el dispositivo de vídeo.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Evento MEStreamSinkDeviceChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651fc34a56ca52cfb9e0b3f20e6e4d6b5366f541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715310"
---
# <a name="mestreamsinkdevicechanged-event"></a><span data-ttu-id="6de67-103">Evento MEStreamSinkDeviceChanged</span><span class="sxs-lookup"><span data-stu-id="6de67-103">MEStreamSinkDeviceChanged event</span></span>

<span data-ttu-id="6de67-104">Generados por los receptores de flujo del representador de vídeo mejorado (EVR) si cambia el dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6de67-104">Raised by the stream sinks of the enhanced video renderer (EVR) if the video device changes.</span></span> <span data-ttu-id="6de67-105">Por ejemplo, el EVR genera este evento cuando recibe un evento [**de \_ \_ cambio de visualización de EC**](../directshow/ec-display-changed.md) .</span><span class="sxs-lookup"><span data-stu-id="6de67-105">For example, the EVR raises this event when it receives an [**EC\_DISPLAY\_CHANGED**](../directshow/ec-display-changed.md) event.</span></span>

<span data-ttu-id="6de67-106">La canalización de Media Foundation responde a este evento al reenviar todas las solicitudes de ejemplo en las que se produjo un error mientras el dispositivo estaba cambiando.</span><span class="sxs-lookup"><span data-stu-id="6de67-106">The Media Foundation pipeline responds to this event by resubmitting all sample requests that failed while the device was changing.</span></span>

## <a name="event-values"></a><span data-ttu-id="6de67-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="6de67-107">Event values</span></span>

<span data-ttu-id="6de67-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="6de67-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6de67-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6de67-109">VARTYPE</span></span>              | <span data-ttu-id="6de67-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6de67-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="6de67-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="6de67-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="6de67-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="6de67-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="6de67-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6de67-113">Requirements</span></span>



| <span data-ttu-id="6de67-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6de67-114">Requirement</span></span> | <span data-ttu-id="6de67-115">Value</span><span class="sxs-lookup"><span data-stu-id="6de67-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de67-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6de67-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6de67-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6de67-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6de67-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6de67-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6de67-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6de67-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6de67-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6de67-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6de67-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6de67-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de67-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6de67-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de67-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6de67-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="6de67-124">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="6de67-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 
