---
description: 'Indica un error grave. Cualquier componente de Media Foundation puede enviar este evento en cualquier momento. Llame a IMFMediaEvent:: GetStatus para obtener el código de error de la operación en la que se produjo un error.'
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Evento MEError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb557dffb2c73a63031a193c331edabe470db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696770"
---
# <a name="meerror-event"></a><span data-ttu-id="e671e-105">Evento MEError</span><span class="sxs-lookup"><span data-stu-id="e671e-105">MEError event</span></span>

<span data-ttu-id="e671e-106">Indica un error grave.</span><span class="sxs-lookup"><span data-stu-id="e671e-106">Signals a serious error.</span></span> <span data-ttu-id="e671e-107">Cualquier componente de Media Foundation puede enviar este evento en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="e671e-107">Any Media Foundation component can send this event at any time.</span></span> <span data-ttu-id="e671e-108">Llame a [**IMFMediaEvent:: getStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) para obtener el código de error de la operación en la que se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="e671e-108">Call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the error code of the operation that failed.</span></span>

## <a name="event-values"></a><span data-ttu-id="e671e-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="e671e-109">Event values</span></span>

<span data-ttu-id="e671e-110">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e671e-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e671e-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e671e-111">VARTYPE</span></span>              | <span data-ttu-id="e671e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e671e-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e671e-113">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="e671e-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e671e-114">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="e671e-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e671e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e671e-115">Remarks</span></span>

<span data-ttu-id="e671e-116">Este evento solo debe usarse para errores inesperados.</span><span class="sxs-lookup"><span data-stu-id="e671e-116">This event should be used only for unexpected errors.</span></span> <span data-ttu-id="e671e-117">No envíe este evento para indicar que se produjo un error en un método asincrónico.</span><span class="sxs-lookup"><span data-stu-id="e671e-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="e671e-118">Si se produce un error en un método asincrónico, se devuelve el código de error en el evento normal para ese método.</span><span class="sxs-lookup"><span data-stu-id="e671e-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="e671e-119">Si se produce un error recuperable durante el streaming, envíe el evento [MENonFatalError](menonfatalerror.md) .</span><span class="sxs-lookup"><span data-stu-id="e671e-119">If a recoverable error occurs during streaming, send the [MENonFatalError](menonfatalerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e671e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e671e-120">Requirements</span></span>



| <span data-ttu-id="e671e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e671e-121">Requirement</span></span> | <span data-ttu-id="e671e-122">Value</span><span class="sxs-lookup"><span data-stu-id="e671e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e671e-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e671e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e671e-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e671e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e671e-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e671e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e671e-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e671e-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e671e-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e671e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e671e-128"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e671e-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e671e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e671e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e671e-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e671e-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




