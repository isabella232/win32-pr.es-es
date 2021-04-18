---
description: 'Se genera cuando el método IMFMediaSession:: Close se completa de forma asincrónica.'
ms.assetid: d1056ce7-5527-428a-8ace-e1c10a2124a5
title: Evento MESessionClosed (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49591e602c06a9beae616ff2a88a2a71241b6e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705993"
---
# <a name="mesessionclosed-event"></a><span data-ttu-id="57665-103">Evento MESessionClosed</span><span class="sxs-lookup"><span data-stu-id="57665-103">MESessionClosed event</span></span>

<span data-ttu-id="57665-104">Se genera cuando el método [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="57665-104">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="57665-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="57665-105">Event values</span></span>

<span data-ttu-id="57665-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="57665-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="57665-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="57665-107">VARTYPE</span></span>              | <span data-ttu-id="57665-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="57665-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="57665-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="57665-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="57665-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="57665-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="57665-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57665-111">Requirements</span></span>



| <span data-ttu-id="57665-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="57665-112">Requirement</span></span> | <span data-ttu-id="57665-113">Value</span><span class="sxs-lookup"><span data-stu-id="57665-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57665-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57665-114">Minimum supported client</span></span><br/> | <span data-ttu-id="57665-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="57665-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="57665-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57665-116">Minimum supported server</span></span><br/> | <span data-ttu-id="57665-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="57665-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57665-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57665-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="57665-119"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57665-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57665-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="57665-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57665-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="57665-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




