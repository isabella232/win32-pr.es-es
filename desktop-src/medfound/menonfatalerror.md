---
description: Se produjo un error no irrecuperable durante el streaming.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Evento MENonFatalError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360523"
---
# <a name="menonfatalerror-event"></a><span data-ttu-id="bbddb-103">Evento MENonFatalError</span><span class="sxs-lookup"><span data-stu-id="bbddb-103">MENonFatalError event</span></span>

<span data-ttu-id="bbddb-104">Se produjo un error no irrecuperable durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="bbddb-104">A non-fatal error occurred during streaming.</span></span> <span data-ttu-id="bbddb-105">Cualquier componente de Media Foundation puede enviar este evento en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="bbddb-105">Any Media Foundation component can send this event at any time.</span></span>

## <a name="event-values"></a><span data-ttu-id="bbddb-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="bbddb-106">Event values</span></span>

<span data-ttu-id="bbddb-107">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="bbddb-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="bbddb-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bbddb-108">VARTYPE</span></span>            | <span data-ttu-id="bbddb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbddb-109">Description</span></span>                                                        |
|--------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bbddb-110">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="bbddb-110">VT\_UI4</span></span><br/> | <span data-ttu-id="bbddb-111">Valor **HRESULT** que describe el error.</span><span class="sxs-lookup"><span data-stu-id="bbddb-111">**HRESULT** value that describes the error.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="bbddb-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="bbddb-112">Attributes</span></span>

<span data-ttu-id="bbddb-113">No hay atributos definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="bbddb-113">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbddb-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbddb-114">Remarks</span></span>

<span data-ttu-id="bbddb-115">Este evento indica un error inesperado pero recuperable durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="bbddb-115">This event signals an unexpected but recoverable error during streaming.</span></span> <span data-ttu-id="bbddb-116">Por ejemplo, un origen multimedia podría enviar este evento si quita un paquete.</span><span class="sxs-lookup"><span data-stu-id="bbddb-116">For example, a media source might send this event if it drops a packet.</span></span>

<span data-ttu-id="bbddb-117">No envíe este evento para indicar que se produjo un error en un método asincrónico.</span><span class="sxs-lookup"><span data-stu-id="bbddb-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="bbddb-118">Si se produce un error en un método asincrónico, se devuelve el código de error en el evento normal para ese método.</span><span class="sxs-lookup"><span data-stu-id="bbddb-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="bbddb-119">Si se produce un error de streaming no recuperable, envíe el evento [MEError](meerror.md) .</span><span class="sxs-lookup"><span data-stu-id="bbddb-119">If a non-recoverable streaming error occurs, send the [MEError](meerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbddb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbddb-120">Requirements</span></span>



| <span data-ttu-id="bbddb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbddb-121">Requirement</span></span> | <span data-ttu-id="bbddb-122">Value</span><span class="sxs-lookup"><span data-stu-id="bbddb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbddb-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbddb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bbddb-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="bbddb-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="bbddb-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbddb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bbddb-126">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bbddb-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="bbddb-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbddb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbddb-128"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbddb-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbddb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbddb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbddb-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bbddb-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




