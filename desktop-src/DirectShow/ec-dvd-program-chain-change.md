---
description: Se envía cuando cambia la cadena de programas actual (PGC).
ms.assetid: 80fcd059-6ab4-4116-ac3a-012c451237b3
title: EC_DVD_PROGRAM_CHAIN_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CHAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: eefd45ac1d147a0409417f215e56a4db490dfdbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679347"
---
# <a name="ec_dvd_program_chain_change"></a><span data-ttu-id="7c8d5-103">\_cambio de \_ cadena de programa de DVD EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="7c8d5-103">EC\_DVD\_PROGRAM\_CHAIN\_CHANGE</span></span>

<span data-ttu-id="7c8d5-104">Se envía cuando cambia la cadena de programas actual (PGC).</span><span class="sxs-lookup"><span data-stu-id="7c8d5-104">Sent when current program chain (PGC) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c8d5-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c8d5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c8d5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7c8d5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7c8d5-107">El nuevo número de cadena de programa (PGCN).</span><span class="sxs-lookup"><span data-stu-id="7c8d5-107">The new program chain number (PGCN).</span></span>

</dd> <dt>

<span data-ttu-id="7c8d5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7c8d5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7c8d5-109">El identificador de configuración regional (LCID) del idioma de audio.</span><span class="sxs-lookup"><span data-stu-id="7c8d5-109">The locale identifier (LCID) of the audio language.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c8d5-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c8d5-110">Remarks</span></span>

<span data-ttu-id="7c8d5-111">Este evento está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7c8d5-111">This event is disabled by default.</span></span> <span data-ttu-id="7c8d5-112">Para habilitar este evento, llame a [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **DVD \_ NotifyPositionChange** en **true**.</span><span class="sxs-lookup"><span data-stu-id="7c8d5-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c8d5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c8d5-113">Requirements</span></span>



| <span data-ttu-id="7c8d5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c8d5-114">Requirement</span></span> | <span data-ttu-id="7c8d5-115">Value</span><span class="sxs-lookup"><span data-stu-id="7c8d5-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c8d5-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c8d5-116">Header</span></span><br/> | <dl> <span data-ttu-id="7c8d5-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c8d5-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c8d5-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c8d5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c8d5-119">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="7c8d5-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7c8d5-120">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="7c8d5-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7c8d5-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="7c8d5-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




