---
description: 'Generado por un flujo multimedia cuando el método IMFMediaSource:: STOP se completa de forma asincrónica.'
ms.assetid: 80280820-b618-43d9-881e-6119dfa36e22
title: Evento MEStreamStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e28060505afc6b16aa6359af21c77cf92df972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706645"
---
# <a name="mestreamstopped-event"></a><span data-ttu-id="e8152-103">Evento MEStreamStopped</span><span class="sxs-lookup"><span data-stu-id="e8152-103">MEStreamStopped event</span></span>

<span data-ttu-id="e8152-104">Generado por un flujo multimedia cuando el método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e8152-104">Raised by a media stream when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="e8152-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="e8152-105">Event values</span></span>

<span data-ttu-id="e8152-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e8152-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e8152-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e8152-107">VARTYPE</span></span>              | <span data-ttu-id="e8152-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8152-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e8152-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="e8152-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e8152-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="e8152-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e8152-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8152-111">Remarks</span></span>

<span data-ttu-id="e8152-112">Cada flujo activo de la presentación envía este evento.</span><span class="sxs-lookup"><span data-stu-id="e8152-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8152-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8152-113">Requirements</span></span>



| <span data-ttu-id="e8152-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8152-114">Requirement</span></span> | <span data-ttu-id="e8152-115">Value</span><span class="sxs-lookup"><span data-stu-id="e8152-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8152-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8152-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e8152-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e8152-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e8152-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8152-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e8152-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8152-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e8152-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8152-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8152-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8152-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8152-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8152-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8152-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8152-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




