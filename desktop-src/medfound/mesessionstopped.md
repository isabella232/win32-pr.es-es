---
description: 'Se genera cuando el método IMFMediaSession:: STOP se completa de forma asincrónica.'
ms.assetid: 9cac9040-f652-4509-bbab-f2a41959d836
title: Evento MESessionStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1bd74c168931cc4ac68ae3c990a156664e4b9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361485"
---
# <a name="mesessionstopped-event"></a><span data-ttu-id="3f408-103">Evento MESessionStopped</span><span class="sxs-lookup"><span data-stu-id="3f408-103">MESessionStopped event</span></span>

<span data-ttu-id="3f408-104">Se genera cuando el método [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3f408-104">Raised when the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="3f408-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="3f408-105">Event values</span></span>

<span data-ttu-id="3f408-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="3f408-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3f408-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3f408-107">VARTYPE</span></span>              | <span data-ttu-id="3f408-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f408-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="3f408-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="3f408-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="3f408-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="3f408-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="3f408-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f408-111">Requirements</span></span>



| <span data-ttu-id="3f408-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f408-112">Requirement</span></span> | <span data-ttu-id="3f408-113">Value</span><span class="sxs-lookup"><span data-stu-id="3f408-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f408-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f408-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3f408-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3f408-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3f408-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f408-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3f408-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f408-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3f408-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f408-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f408-119"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f408-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f408-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f408-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f408-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f408-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




