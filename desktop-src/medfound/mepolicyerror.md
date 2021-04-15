---
description: Generado por una salida de confianza si se produce un error durante la aplicación de la Directiva de salida.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: Evento MEPolicyError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b75083974ee0e76d7d8e21f0a2c83c2feee8d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715665"
---
# <a name="mepolicyerror-event"></a><span data-ttu-id="0fc84-103">Evento MEPolicyError</span><span class="sxs-lookup"><span data-stu-id="0fc84-103">MEPolicyError event</span></span>

<span data-ttu-id="0fc84-104">Generado por una salida de confianza si se produce un error durante la aplicación de la Directiva de salida.</span><span class="sxs-lookup"><span data-stu-id="0fc84-104">Raised by a trusted output if an error occurs while enforcing the output policy.</span></span>

<span data-ttu-id="0fc84-105">Si la sesión multimedia recibe este evento, detiene la reproducción y reenvía el evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0fc84-105">If the Media Session receives this event, it stops playback and forwards the event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="0fc84-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="0fc84-106">Event values</span></span>

<span data-ttu-id="0fc84-107">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="0fc84-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0fc84-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0fc84-108">VARTYPE</span></span>              | <span data-ttu-id="0fc84-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fc84-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="0fc84-110">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="0fc84-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0fc84-111">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="0fc84-111">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0fc84-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fc84-112">Remarks</span></span>

<span data-ttu-id="0fc84-113">Los valores posibles recuperados de [**IMFMediaEvent:: getStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) incluyen los siguientes.</span><span class="sxs-lookup"><span data-stu-id="0fc84-113">Possible values retrieved from [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) include the following.</span></span>



| <span data-ttu-id="0fc84-114">Value</span><span class="sxs-lookup"><span data-stu-id="0fc84-114">Value</span></span>                      | <span data-ttu-id="0fc84-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fc84-115">Description</span></span>                                                    |
|----------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0fc84-116">\_Directiva MF \_ E \_ no admitida</span><span class="sxs-lookup"><span data-stu-id="0fc84-116">MF\_E\_POLICY\_UNSUPPORTED</span></span> | <span data-ttu-id="0fc84-117">La salida de confianza no admite la Directiva de salida actual.</span><span class="sxs-lookup"><span data-stu-id="0fc84-117">The trusted output does not support the current output policy.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0fc84-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fc84-118">Requirements</span></span>



| <span data-ttu-id="0fc84-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fc84-119">Requirement</span></span> | <span data-ttu-id="0fc84-120">Value</span><span class="sxs-lookup"><span data-stu-id="0fc84-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc84-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fc84-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0fc84-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0fc84-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0fc84-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fc84-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0fc84-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0fc84-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0fc84-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fc84-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fc84-126"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fc84-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fc84-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fc84-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc84-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0fc84-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




