---
description: 'Se genera después de que el método IMFMediaSession:: SetTopology se complete de forma asincrónica. La sesión multimedia genera este evento después de resolver la topología en una topología completa y pone en cola la topología para la reproducción.'
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Evento MESessionTopologySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001514"
---
# <a name="mesessiontopologyset-event"></a><span data-ttu-id="a0d61-104">Evento MESessionTopologySet</span><span class="sxs-lookup"><span data-stu-id="a0d61-104">MESessionTopologySet event</span></span>

<span data-ttu-id="a0d61-105">Se genera después de que el método [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se complete de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="a0d61-105">Raised after the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="a0d61-106">La sesión multimedia genera este evento después de resolver la topología en una topología completa y pone en cola la topología para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="a0d61-106">The Media Session raises this event after it resolves the topology into a full topology and queues the topology for playback.</span></span>

## <a name="event-values"></a><span data-ttu-id="a0d61-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="a0d61-107">Event values</span></span>

<span data-ttu-id="a0d61-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="a0d61-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a0d61-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a0d61-109">VARTYPE</span></span>                | <span data-ttu-id="a0d61-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0d61-110">Description</span></span>                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d61-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="a0d61-111">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="a0d61-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="a0d61-112">No event data.</span></span><br/> <br/>                                                                    |
| <span data-ttu-id="a0d61-113">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="a0d61-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="a0d61-114">Puntero a la interfaz [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topología completa.</span><span class="sxs-lookup"><span data-stu-id="a0d61-114">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the full topology.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="a0d61-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a0d61-115">Examples</span></span>

<span data-ttu-id="a0d61-116">En el ejemplo siguiente se recupera el puntero [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de un evento MESessionTopologySet.</span><span class="sxs-lookup"><span data-stu-id="a0d61-116">The following example retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from an MESessionTopologySet event.</span></span>


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="a0d61-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0d61-117">Requirements</span></span>



| <span data-ttu-id="a0d61-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0d61-118">Requirement</span></span> | <span data-ttu-id="a0d61-119">Value</span><span class="sxs-lookup"><span data-stu-id="a0d61-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d61-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0d61-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a0d61-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a0d61-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0d61-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0d61-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a0d61-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0d61-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a0d61-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0d61-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0d61-125"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0d61-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0d61-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0d61-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0d61-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a0d61-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




