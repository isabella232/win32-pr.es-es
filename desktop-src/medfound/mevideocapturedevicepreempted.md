---
description: Enviado por el IMFMediaSource que encapsula el dispositivo para indicar que el dispositivo se ha adelantado.
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: Evento MEVideoCaptureDevicePreempted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3968c0641d954741474b1d5ec7ffaa11dcad5f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687224"
---
# <a name="mevideocapturedevicepreempted-event"></a><span data-ttu-id="4d7ba-103">Evento MEVideoCaptureDevicePreempted</span><span class="sxs-lookup"><span data-stu-id="4d7ba-103">MEVideoCaptureDevicePreempted event</span></span>

<span data-ttu-id="4d7ba-104">Enviado por el [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula el dispositivo para indicar que el dispositivo se ha adelantado.</span><span class="sxs-lookup"><span data-stu-id="4d7ba-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been preempted.</span></span>

## <a name="event-values"></a><span data-ttu-id="4d7ba-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="4d7ba-105">Event values</span></span>

<span data-ttu-id="4d7ba-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4d7ba-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4d7ba-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4d7ba-107">VARTYPE</span></span>               | <span data-ttu-id="4d7ba-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d7ba-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="4d7ba-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="4d7ba-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="4d7ba-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="4d7ba-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4d7ba-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d7ba-111">Remarks</span></span>

<span data-ttu-id="4d7ba-112">Este evento lo envía el [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d7ba-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d7ba-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d7ba-113">Requirements</span></span>



| <span data-ttu-id="4d7ba-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d7ba-114">Requirement</span></span> | <span data-ttu-id="4d7ba-115">Value</span><span class="sxs-lookup"><span data-stu-id="4d7ba-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7ba-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d7ba-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4d7ba-117">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d7ba-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="4d7ba-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d7ba-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4d7ba-119">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d7ba-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4d7ba-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d7ba-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d7ba-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ba-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d7ba-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d7ba-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7ba-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4d7ba-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




