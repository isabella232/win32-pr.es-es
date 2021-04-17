---
description: Indica el principio de cada unidad de objeto de vídeo (VOBU), un segmento de vídeo de 0,4 a 1,0 segundos de longitud.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653584"
---
# <a name="ec_dvd_current_time"></a><span data-ttu-id="7826c-103">\_ \_ hora actual del DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="7826c-103">EC\_DVD\_CURRENT\_TIME</span></span>

<span data-ttu-id="7826c-104">Indica el principio de cada unidad de objeto de vídeo (VOBU), un segmento de vídeo de 0,4 a 1,0 segundos de longitud.</span><span class="sxs-lookup"><span data-stu-id="7826c-104">Signals the beginning of every video object unit (VOBU), a video segment which is 0.4 to 1.0 seconds in length.</span></span>

## <a name="parameters"></a><span data-ttu-id="7826c-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7826c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7826c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7826c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7826c-107">Valor **DWORD** que indica el código de tiempo de reproducción actual en un formato de horas, minutos, segundos y fotogramas (HH: mm: SS: FF) con código binario.</span><span class="sxs-lookup"><span data-stu-id="7826c-107">**DWORD** value indicating the current playback timecode in a binary coded decimal (BCD) hours, minutes, seconds, frames (HH:MM:SS:FF) format.</span></span> <span data-ttu-id="7826c-108">Miembro de la estructura de [**\_ código de tiempo de DVD**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) .</span><span class="sxs-lookup"><span data-stu-id="7826c-108">Member of the [**DVD\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7826c-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7826c-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7826c-110">Valor booleano (**bool**) que indica el código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="7826c-110">Boolean (**BOOL**) value indicating the timecode.</span></span> <span data-ttu-id="7826c-111">Cero (0) indica 25 fotogramas por segundo, mientras que 1 indica 30 fotogramas por segundo (no quitado).</span><span class="sxs-lookup"><span data-stu-id="7826c-111">Zero (0) indicates 25 frames per second while 1 indicates 30 frames per second (nondropped).</span></span> <span data-ttu-id="7826c-112">Un valor de 2 indica que no se puede determinar la hora de reproducción.</span><span class="sxs-lookup"><span data-stu-id="7826c-112">A value of 2 indicates the playback time cannot be determined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7826c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7826c-113">Remarks</span></span>

<span data-ttu-id="7826c-114">Solo las películas lineales simples señalan este evento.</span><span class="sxs-lookup"><span data-stu-id="7826c-114">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="7826c-115">Este evento se desencadena en el dominio de título.</span><span class="sxs-lookup"><span data-stu-id="7826c-115">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="7826c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7826c-116">Requirements</span></span>



| <span data-ttu-id="7826c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7826c-117">Requirement</span></span> | <span data-ttu-id="7826c-118">Value</span><span class="sxs-lookup"><span data-stu-id="7826c-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7826c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7826c-119">Header</span></span><br/> | <dl> <span data-ttu-id="7826c-120"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7826c-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7826c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7826c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7826c-122">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="7826c-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7826c-123">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="7826c-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7826c-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="7826c-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




