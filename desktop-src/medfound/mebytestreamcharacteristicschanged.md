---
description: Lo envía una secuencia de bytes cuando las características de la secuencia de bytes han cambiado.
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: Evento MEByteStreamCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720428"
---
# <a name="mebytestreamcharacteristicschanged-event"></a><span data-ttu-id="8f62c-103">Evento MEByteStreamCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="8f62c-103">MEByteStreamCharacteristicsChanged event</span></span>

<span data-ttu-id="8f62c-104">Lo envía una secuencia de bytes cuando las características de la secuencia de bytes han cambiado.</span><span class="sxs-lookup"><span data-stu-id="8f62c-104">Sent by a byte stream when the characteristics of the byte stream have changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="8f62c-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="8f62c-105">Event values</span></span>

<span data-ttu-id="8f62c-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="8f62c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8f62c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8f62c-107">VARTYPE</span></span>               | <span data-ttu-id="8f62c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f62c-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="8f62c-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="8f62c-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="8f62c-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="8f62c-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8f62c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f62c-111">Remarks</span></span>

<span data-ttu-id="8f62c-112">Este evento indica que una o varias de las características siguientes han cambiado:</span><span class="sxs-lookup"><span data-stu-id="8f62c-112">This event indicates that one or more of the following characteristics has changed:</span></span>

-   <span data-ttu-id="8f62c-113">Marcas de capacidad ([**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))</span><span class="sxs-lookup"><span data-stu-id="8f62c-113">Capability flags ([**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))</span></span>
-   <span data-ttu-id="8f62c-114">Marca de fin de secuencia ([**IMFByteStream:: IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))</span><span class="sxs-lookup"><span data-stu-id="8f62c-114">End-of-stream flag ([**IMFByteStream::IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))</span></span>
-   <span data-ttu-id="8f62c-115">Longitud ([**IMFByteStream:: GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))</span><span class="sxs-lookup"><span data-stu-id="8f62c-115">Length ([**IMFByteStream::GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))</span></span>

<span data-ttu-id="8f62c-116">No todas las implementaciones de [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) admiten este evento.</span><span class="sxs-lookup"><span data-stu-id="8f62c-116">Not all [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) implementations support this event.</span></span> <span data-ttu-id="8f62c-117">Para recibir el evento, consulte el objeto de secuencia de bytes para la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="8f62c-117">To receive the event, query the byte-stream object for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f62c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f62c-118">Requirements</span></span>



| <span data-ttu-id="8f62c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f62c-119">Requirement</span></span> | <span data-ttu-id="8f62c-120">Value</span><span class="sxs-lookup"><span data-stu-id="8f62c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f62c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f62c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8f62c-122">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f62c-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="8f62c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f62c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8f62c-124">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f62c-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8f62c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f62c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f62c-126"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f62c-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f62c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f62c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f62c-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8f62c-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




