---
description: Indica que un origen multimedia ha dejado de almacenar en búfer los datos.
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: Evento MEBufferingStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e996ec160f57ec598196b388170741705adb9a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360459"
---
# <a name="mebufferingstopped-event"></a><span data-ttu-id="79425-103">Evento MEBufferingStopped</span><span class="sxs-lookup"><span data-stu-id="79425-103">MEBufferingStopped event</span></span>

<span data-ttu-id="79425-104">Indica que un origen multimedia ha dejado de almacenar en búfer los datos.</span><span class="sxs-lookup"><span data-stu-id="79425-104">Signals that a media source has stopped buffering data.</span></span>

<span data-ttu-id="79425-105">Un origen multimedia lo envía cuando detiene el almacenamiento en búfer de los datos después de enviar el evento [MEBufferingStarted](mebufferingstarted.md) .</span><span class="sxs-lookup"><span data-stu-id="79425-105">A media source sends this when it stops buffering data after sending the [MEBufferingStarted](mebufferingstarted.md) event.</span></span>

<span data-ttu-id="79425-106">Los flujos de bytes que implementan la interfaz [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) también envían este evento.</span><span class="sxs-lookup"><span data-stu-id="79425-106">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="79425-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="79425-107">Event values</span></span>

<span data-ttu-id="79425-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="79425-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="79425-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="79425-109">VARTYPE</span></span>              | <span data-ttu-id="79425-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="79425-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="79425-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="79425-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="79425-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="79425-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="79425-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79425-113">Remarks</span></span>

<span data-ttu-id="79425-114">Cuando la sesión multimedia recibe este evento, reinicia el reloj de la presentación.</span><span class="sxs-lookup"><span data-stu-id="79425-114">When the Media Session receives this event, it restarts the presentation clock.</span></span> <span data-ttu-id="79425-115">La sesión multimedia también reenvía el evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="79425-115">The Media Session also forwards the event to the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="79425-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79425-116">Requirements</span></span>



| <span data-ttu-id="79425-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="79425-117">Requirement</span></span> | <span data-ttu-id="79425-118">Value</span><span class="sxs-lookup"><span data-stu-id="79425-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79425-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79425-119">Minimum supported client</span></span><br/> | <span data-ttu-id="79425-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="79425-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="79425-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79425-121">Minimum supported server</span></span><br/> | <span data-ttu-id="79425-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="79425-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="79425-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79425-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="79425-124"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79425-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79425-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="79425-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79425-126">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79425-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




