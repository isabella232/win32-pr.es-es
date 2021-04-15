---
description: Generado por un componente de canalización cuando cambia la Directiva de salida para la secuencia. Este evento solo se aplica al contenido protegido.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Evento MEPolicyChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6827c44958e2df016365a8caa9a66f1aad9a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715667"
---
# <a name="mepolicychanged-event"></a><span data-ttu-id="e2509-104">Evento MEPolicyChanged</span><span class="sxs-lookup"><span data-stu-id="e2509-104">MEPolicyChanged event</span></span>

<span data-ttu-id="e2509-105">Generado por un componente de canalización cuando cambia la Directiva de salida para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e2509-105">Raised by a pipeline component when the output policy for the stream changes.</span></span> <span data-ttu-id="e2509-106">Este evento solo se aplica al contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="e2509-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="e2509-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="e2509-107">Event values</span></span>

<span data-ttu-id="e2509-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e2509-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e2509-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e2509-109">VARTYPE</span></span>                | <span data-ttu-id="e2509-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2509-110">Description</span></span>                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2509-111">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="e2509-111">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="e2509-112">Puntero a la interfaz [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) de la nueva Directiva para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e2509-112">Pointer to the [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) interface of the new policy for the stream.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e2509-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2509-113">Remarks</span></span>

<span data-ttu-id="e2509-114">Todas las salidas de confianza deben controlar este evento.</span><span class="sxs-lookup"><span data-stu-id="e2509-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="e2509-115">Media Foundation transformaciones (MFTs) reciben este evento a través del método [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) .</span><span class="sxs-lookup"><span data-stu-id="e2509-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="e2509-116">Los receptores de medios reciben este evento a través del método [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="e2509-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="e2509-117">La salida de confianza debe aplicar la nueva Directiva o devolver el código de error MF \_ E \_ directiva \_ no compatible.</span><span class="sxs-lookup"><span data-stu-id="e2509-117">The trusted output must apply the new policy or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2509-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2509-118">Requirements</span></span>



| <span data-ttu-id="e2509-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2509-119">Requirement</span></span> | <span data-ttu-id="e2509-120">Value</span><span class="sxs-lookup"><span data-stu-id="e2509-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2509-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2509-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e2509-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="e2509-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="e2509-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2509-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e2509-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="e2509-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="e2509-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2509-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2509-126"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2509-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2509-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2509-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2509-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2509-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




