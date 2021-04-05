---
description: Generado por un componente de canalización cuando cambia la configuración de uno de los esquemas de protección de salida. Este evento solo se aplica al contenido protegido.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Evento MEContentProtectionMessage (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f96ac75711559881232ced4cec6bfca2bc030c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811036"
---
# <a name="mecontentprotectionmessage-event"></a><span data-ttu-id="6ecce-104">Evento MEContentProtectionMessage</span><span class="sxs-lookup"><span data-stu-id="6ecce-104">MEContentProtectionMessage event</span></span>

<span data-ttu-id="6ecce-105">Generado por un componente de canalización cuando cambia la configuración de uno de los esquemas de protección de salida.</span><span class="sxs-lookup"><span data-stu-id="6ecce-105">Raised by a pipeline component when the configuration changes for one of the output protection schemes.</span></span> <span data-ttu-id="6ecce-106">Este evento solo se aplica al contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="6ecce-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="6ecce-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="6ecce-107">Event values</span></span>

<span data-ttu-id="6ecce-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="6ecce-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6ecce-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6ecce-109">VARTYPE</span></span>              | <span data-ttu-id="6ecce-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ecce-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="6ecce-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="6ecce-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="6ecce-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="6ecce-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6ecce-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ecce-113">Remarks</span></span>

<span data-ttu-id="6ecce-114">Todas las salidas de confianza deben controlar este evento.</span><span class="sxs-lookup"><span data-stu-id="6ecce-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="6ecce-115">Media Foundation transformaciones (MFTs) reciben este evento a través del método [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) .</span><span class="sxs-lookup"><span data-stu-id="6ecce-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="6ecce-116">Los receptores de medios reciben este evento a través del método [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="6ecce-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="6ecce-117">La salida de confianza debe aplicar los cambios de la Directiva o devolver el código de error MF \_ E \_ directiva \_ no compatible.</span><span class="sxs-lookup"><span data-stu-id="6ecce-117">The trusted output must apply the policy changes or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

<span data-ttu-id="6ecce-118">Los datos y atributos del evento dependen del sistema de protección de contenido en uso.</span><span class="sxs-lookup"><span data-stu-id="6ecce-118">The event data and attributes depend on the content protection system in use.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ecce-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ecce-119">Requirements</span></span>



| <span data-ttu-id="6ecce-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ecce-120">Requirement</span></span> | <span data-ttu-id="6ecce-121">Value</span><span class="sxs-lookup"><span data-stu-id="6ecce-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ecce-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ecce-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6ecce-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="6ecce-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="6ecce-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ecce-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6ecce-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="6ecce-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="6ecce-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ecce-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ecce-127"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ecce-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ecce-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ecce-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ecce-129">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ecce-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




