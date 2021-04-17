---
description: Indica el principio de cualquier todavía (PGC, Cell o VOBU).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653404"
---
# <a name="ec_dvd_still_on"></a><span data-ttu-id="69802-103">\_DVD \_ de EC todavía \_ encendido</span><span class="sxs-lookup"><span data-stu-id="69802-103">EC\_DVD\_STILL\_ON</span></span>

<span data-ttu-id="69802-104">Indica el principio de cualquier todavía (PGC, Cell o VOBU).</span><span class="sxs-lookup"><span data-stu-id="69802-104">Signals the beginning of any still (PGC, Cell, or VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="69802-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69802-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69802-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="69802-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="69802-107">Valor booleano (**bool**) que indica si los botones están disponibles.</span><span class="sxs-lookup"><span data-stu-id="69802-107">Boolean (**BOOL**) value indicating whether buttons are available.</span></span> <span data-ttu-id="69802-108">Cero (0) indica que los botones están disponibles, por lo que el método [**IDvdControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) no funcionará.</span><span class="sxs-lookup"><span data-stu-id="69802-108">Zero (0) indicates buttons are available so the [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) method won't work.</span></span> <span data-ttu-id="69802-109">Uno (1) indica que no hay botones disponibles, por lo que **IDvdControl2:: StillOff** funcionará.</span><span class="sxs-lookup"><span data-stu-id="69802-109">One (1) indicates no buttons are available, so **IDvdControl2::StillOff** will work.</span></span>

</dd> <dt>

<span data-ttu-id="69802-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="69802-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="69802-111">Valor **DWORD** que indica el número de segundos que sigue siendo el último.</span><span class="sxs-lookup"><span data-stu-id="69802-111">**DWORD** value indicating the number of seconds the still will last.</span></span> <span data-ttu-id="69802-112">0xFFFFFFFF indica un infinito fijo, lo que significa esperar hasta que el usuario presione un botón o hasta que la aplicación llame a [**IDvdControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span><span class="sxs-lookup"><span data-stu-id="69802-112">0xFFFFFFFF indicates an infinite still, meaning wait until the user presses a button or until the application calls [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69802-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69802-113">Remarks</span></span>

<span data-ttu-id="69802-114">Todas las combinaciones de botones y siguen siendo posibles (botones en con la opción con el mismo botón activado, botones en con todavía desactivado, botón desactivado con el botón sin conexión).</span><span class="sxs-lookup"><span data-stu-id="69802-114">All combinations of buttons and still are possible (buttons on with still on, buttons on with still off, button off with still on, button off with still off).</span></span>

<span data-ttu-id="69802-115">Este evento se desencadena en todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="69802-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="69802-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69802-116">Requirements</span></span>



| <span data-ttu-id="69802-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="69802-117">Requirement</span></span> | <span data-ttu-id="69802-118">Value</span><span class="sxs-lookup"><span data-stu-id="69802-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69802-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69802-119">Header</span></span><br/> | <dl> <span data-ttu-id="69802-120"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69802-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69802-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="69802-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69802-122">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="69802-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="69802-123">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="69802-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="69802-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="69802-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




