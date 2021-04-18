---
description: 'Generado por un origen multimedia cuando el método IMFMediaSource:: STOP se completa de forma asincrónica.'
ms.assetid: 0eda9aa1-3aad-43ac-9d87-ab96e4ac319d
title: Evento MESourceStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d08909a95cf1c867c5d8392425f25565b5a2728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715311"
---
# <a name="mesourcestopped-event"></a><span data-ttu-id="7f32c-103">Evento MESourceStopped</span><span class="sxs-lookup"><span data-stu-id="7f32c-103">MESourceStopped event</span></span>

<span data-ttu-id="7f32c-104">Generado por un origen multimedia cuando el método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7f32c-104">Raised by a media source when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="7f32c-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="7f32c-105">Event values</span></span>

<span data-ttu-id="7f32c-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="7f32c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7f32c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7f32c-107">VARTYPE</span></span>              | <span data-ttu-id="7f32c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f32c-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="7f32c-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="7f32c-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="7f32c-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="7f32c-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="7f32c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f32c-111">Requirements</span></span>



| <span data-ttu-id="7f32c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f32c-112">Requirement</span></span> | <span data-ttu-id="7f32c-113">Value</span><span class="sxs-lookup"><span data-stu-id="7f32c-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f32c-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f32c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7f32c-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7f32c-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7f32c-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f32c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7f32c-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f32c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7f32c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f32c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f32c-119"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f32c-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f32c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f32c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f32c-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f32c-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




