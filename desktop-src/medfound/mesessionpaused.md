---
description: Se genera cuando el método IMFMediaSession::P ause se completa de forma asincrónica.
ms.assetid: 72546082-83ec-4481-a24f-e82bd6c88859
title: Evento MESessionPaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd3e8ef60426f83203cfffae3a75febfdf7032d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155584"
---
# <a name="mesessionpaused-event"></a><span data-ttu-id="42f9a-103">Evento MESessionPaused</span><span class="sxs-lookup"><span data-stu-id="42f9a-103">MESessionPaused event</span></span>

<span data-ttu-id="42f9a-104">Se genera cuando el método [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="42f9a-104">Raised when the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="42f9a-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="42f9a-105">Event values</span></span>

<span data-ttu-id="42f9a-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="42f9a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="42f9a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="42f9a-107">VARTYPE</span></span>              | <span data-ttu-id="42f9a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="42f9a-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="42f9a-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="42f9a-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="42f9a-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="42f9a-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="42f9a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42f9a-111">Requirements</span></span>



| <span data-ttu-id="42f9a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="42f9a-112">Requirement</span></span> | <span data-ttu-id="42f9a-113">Value</span><span class="sxs-lookup"><span data-stu-id="42f9a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f9a-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42f9a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="42f9a-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="42f9a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42f9a-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42f9a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="42f9a-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="42f9a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42f9a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42f9a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="42f9a-119"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42f9a-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f9a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="42f9a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f9a-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42f9a-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




