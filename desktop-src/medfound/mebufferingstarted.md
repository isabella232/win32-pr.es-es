---
description: Indica que un origen multimedia ha empezado a almacenar en búfer los datos.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Evento MEBufferingStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb3baf8e66d44eb67ee4c1bbc54ae2e197db081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720429"
---
# <a name="mebufferingstarted-event"></a><span data-ttu-id="6704a-103">Evento MEBufferingStarted</span><span class="sxs-lookup"><span data-stu-id="6704a-103">MEBufferingStarted event</span></span>

<span data-ttu-id="6704a-104">Indica que un origen multimedia ha empezado a almacenar en búfer los datos.</span><span class="sxs-lookup"><span data-stu-id="6704a-104">Signals that a media source has started to buffer data.</span></span>

<span data-ttu-id="6704a-105">Un origen multimedia puede enviar este evento si el origen almacena en búfer los datos mientras se ejecuta la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6704a-105">A media source can send this event if the source buffers data while the Media Session is running.</span></span> <span data-ttu-id="6704a-106">Cuando la sesión multimedia recibe este evento, detiene el reloj de la presentación hasta que el origen del medio envía el evento [MEBufferingStopped](mebufferingstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="6704a-106">When the Media Session receives this event, it pauses the presentation clock until the media source sends the [MEBufferingStopped](mebufferingstopped.md) event.</span></span> <span data-ttu-id="6704a-107">La sesión multimedia también reenvía el evento MEBufferingStarted a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6704a-107">The Media Session also forwards the MEBufferingStarted event to the application.</span></span>

<span data-ttu-id="6704a-108">Los flujos de bytes que implementan la interfaz [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) también envían este evento.</span><span class="sxs-lookup"><span data-stu-id="6704a-108">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="6704a-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="6704a-109">Event values</span></span>

<span data-ttu-id="6704a-110">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="6704a-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6704a-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6704a-111">VARTYPE</span></span>              | <span data-ttu-id="6704a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6704a-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="6704a-113">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="6704a-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="6704a-114">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="6704a-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6704a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6704a-115">Remarks</span></span>

<span data-ttu-id="6704a-116">Si un origen multimedia envía el evento MEBufferingStarted, debe enviar el evento [MEBufferingStopped](mebufferingstopped.md) cuando detenga el almacenamiento en búfer de los datos.</span><span class="sxs-lookup"><span data-stu-id="6704a-116">If a media source sends the MEBufferingStarted event, it must send the [MEBufferingStopped](mebufferingstopped.md) event when it stops buffering data.</span></span> <span data-ttu-id="6704a-117">El origen multimedia debe enviar un evento MEBufferingStopped coincidente para cada evento MEBufferingStarted.</span><span class="sxs-lookup"><span data-stu-id="6704a-117">The media source must send a matching MEBufferingStopped event for every MEBufferingStarted event.</span></span> <span data-ttu-id="6704a-118">El origen multimedia no debe reenviar estos eventos antes de que se llame al método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) del origen o después de que se llame al método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) del origen.</span><span class="sxs-lookup"><span data-stu-id="6704a-118">The media source should not forward these events before the source's [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called, or after the source's [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method is called.</span></span>

<span data-ttu-id="6704a-119">Si va a realizar el streaming desde el Media Foundation origen de red, puede obtener el progreso del almacenamiento en búfer consultando la estadística del **\_ \_ identificador de BUFFERPROGRESS de MFNETSOURCE** .</span><span class="sxs-lookup"><span data-stu-id="6704a-119">If you are streaming from the Media Foundation network source, you can get the buffering progress by querying the **MFNETSOURCE\_BUFFERPROGRESS\_ID** statistic.</span></span> <span data-ttu-id="6704a-120">Para obtener más información, consulte [**MFNETSOURCE \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="6704a-120">For more information, see [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>

## <a name="examples"></a><span data-ttu-id="6704a-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6704a-121">Examples</span></span>


```C++
HRESULT GetBufferProgress(IMFMediaSession *pSession, DWORD *pProgress)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_BUFFERPROGRESS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pProgress = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="6704a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6704a-122">Requirements</span></span>



| <span data-ttu-id="6704a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6704a-123">Requirement</span></span> | <span data-ttu-id="6704a-124">Value</span><span class="sxs-lookup"><span data-stu-id="6704a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6704a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6704a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6704a-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6704a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6704a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6704a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6704a-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6704a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6704a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6704a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6704a-130"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6704a-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6704a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6704a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6704a-132">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6704a-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="6704a-133">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6704a-133">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




