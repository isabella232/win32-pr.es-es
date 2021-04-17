---
description: Enviado por el IMFMediaSource que encapsula el dispositivo para indicar que el dispositivo se ha quitado.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: Evento MEVideoCaptureDeviceRemoved (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3276f53f86bdce78825b94828577eab9e40954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678161"
---
# <a name="mevideocapturedeviceremoved-event"></a><span data-ttu-id="24657-103">Evento MEVideoCaptureDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="24657-103">MEVideoCaptureDeviceRemoved event</span></span>

<span data-ttu-id="24657-104">Enviado por el [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula el dispositivo para indicar que el dispositivo se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="24657-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been removed.</span></span>

## <a name="event-values"></a><span data-ttu-id="24657-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="24657-105">Event values</span></span>

<span data-ttu-id="24657-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="24657-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="24657-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="24657-107">VARTYPE</span></span>               | <span data-ttu-id="24657-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="24657-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="24657-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="24657-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="24657-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="24657-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="24657-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24657-111">Remarks</span></span>

<span data-ttu-id="24657-112">Este evento lo envía el [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24657-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="24657-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24657-113">Requirements</span></span>



| <span data-ttu-id="24657-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="24657-114">Requirement</span></span> | <span data-ttu-id="24657-115">Value</span><span class="sxs-lookup"><span data-stu-id="24657-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24657-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24657-116">Minimum supported client</span></span><br/> | <span data-ttu-id="24657-117">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="24657-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="24657-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24657-118">Minimum supported server</span></span><br/> | <span data-ttu-id="24657-119">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="24657-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24657-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24657-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="24657-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24657-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24657-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="24657-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24657-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24657-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




