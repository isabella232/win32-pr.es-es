---
description: Proporciona comentarios al administrador de calidad sobre la calidad de la reproducción.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Evento MEQualityNotify (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d8f486bfebfd137ba341176af0fdad257776df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544387"
---
# <a name="mequalitynotify-event"></a><span data-ttu-id="48443-103">Evento MEQualityNotify</span><span class="sxs-lookup"><span data-stu-id="48443-103">MEQualityNotify event</span></span>

<span data-ttu-id="48443-104">Proporciona comentarios al administrador de calidad sobre la calidad de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="48443-104">Provides feedback to the quality manager about playback quality.</span></span>

## <a name="event-values"></a><span data-ttu-id="48443-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="48443-105">Event values</span></span>

<span data-ttu-id="48443-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="48443-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="48443-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="48443-107">VARTYPE</span></span>           | <span data-ttu-id="48443-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="48443-108">Description</span></span>                         |
|-------------------|-------------------------------------|
| <span data-ttu-id="48443-109">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="48443-109">VT\_I8</span></span><br/> | <span data-ttu-id="48443-110">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="48443-110">See Remarks.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="48443-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48443-111">Remarks</span></span>

<span data-ttu-id="48443-112">Este evento es desencadenado por algunos componentes de canalización.</span><span class="sxs-lookup"><span data-stu-id="48443-112">This event is raised by some pipeline components.</span></span> <span data-ttu-id="48443-113">La sesión multimedia reenvía el evento al administrador de calidad mediante una llamada al método [**IMFQualityManager:: NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) .</span><span class="sxs-lookup"><span data-stu-id="48443-113">The Media Session forwards the event to the quality manager by calling the [**IMFQualityManager::NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) method.</span></span>

<span data-ttu-id="48443-114">El tipo extendido del evento indica el significado de los datos del evento.</span><span class="sxs-lookup"><span data-stu-id="48443-114">The event's extended type indicates the meaning of the event data.</span></span>



| <span data-ttu-id="48443-115">Tipo extendido</span><span class="sxs-lookup"><span data-stu-id="48443-115">Extended type</span></span>                            | <span data-ttu-id="48443-116">Datos de evento</span><span class="sxs-lookup"><span data-stu-id="48443-116">Event data</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48443-117">\_latencia de \_ procesamiento de notificaciones de calidad MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="48443-117">MF\_QUALITY\_NOTIFY\_PROCESSING\_LATENCY</span></span> | <span data-ttu-id="48443-118">Latencia de procesamiento aproximada introducida por el componente, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="48443-118">Approximate processing latency introduced by the component, in 100-nanosecond units.</span></span><br/> <span data-ttu-id="48443-119">La latencia de procesamiento es la cantidad de latencia que un componente introduce en la canalización mediante el procesamiento de un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="48443-119">Processing latency is the amount of latency that a component introduces into the pipeline by processing a sample.</span></span> <span data-ttu-id="48443-120">En algunos casos, la latencia no se puede derivar simplemente examinando las llamadas a [**IMFQualityManager:: NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) y [**IMFQualityManager:: NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span><span class="sxs-lookup"><span data-stu-id="48443-120">In some cases, the latency cannot be derived simply by looking at the calls to [**IMFQualityManager::NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) and [**IMFQualityManager::NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span></span> <span data-ttu-id="48443-121">Por ejemplo, puede que no haya una correspondencia uno a uno entre los ejemplos de entrada y los ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="48443-121">For example, there may not be a one-to-one correspondence between input samples and output samples.</span></span> <span data-ttu-id="48443-122">En este caso, el componente podría enviar un evento MEQualityNotify con la latencia de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="48443-122">In this case, the component might send an MEQualityNotify event with the processing latency.</span></span> <span data-ttu-id="48443-123">Si la latencia de procesamiento cambia, el componente puede enviar un nuevo evento en cualquier momento durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="48443-123">If the processing latency changes, the component can send a new event at any time during streaming.</span></span><br/> |
| <span data-ttu-id="48443-124">retardo de muestra de notificación de \_ calidad MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="48443-124">MF\_QUALITY\_NOTIFY\_SAMPLE\_LAG</span></span>         | <span data-ttu-id="48443-125">Tiempo de retardo para el ejemplo, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="48443-125">Lag time for the sample, in 100-nanosecond units.</span></span> <span data-ttu-id="48443-126">Si el valor es positivo, el ejemplo estaba atrasado.</span><span class="sxs-lookup"><span data-stu-id="48443-126">If the value is positive, the sample was late.</span></span> <span data-ttu-id="48443-127">Si el valor es negativo, el ejemplo era temprano.</span><span class="sxs-lookup"><span data-stu-id="48443-127">If the value is negative, the sample was early.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="48443-128">Para obtener el tipo extendido, llame a [**IMFMediaEvent:: GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="48443-128">To get the extended type, call [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

<span data-ttu-id="48443-129">No es necesario que los componentes de canalización envíen este evento.</span><span class="sxs-lookup"><span data-stu-id="48443-129">Pipeline components are not required to send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="48443-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48443-130">Requirements</span></span>



| <span data-ttu-id="48443-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="48443-131">Requirement</span></span> | <span data-ttu-id="48443-132">Value</span><span class="sxs-lookup"><span data-stu-id="48443-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48443-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48443-133">Minimum supported client</span></span><br/> | <span data-ttu-id="48443-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="48443-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="48443-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48443-135">Minimum supported server</span></span><br/> | <span data-ttu-id="48443-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="48443-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="48443-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48443-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="48443-138"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48443-138"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48443-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="48443-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48443-140">**IMFQualityManager**</span><span class="sxs-lookup"><span data-stu-id="48443-140">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[<span data-ttu-id="48443-141">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="48443-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




