---
description: Se envía cuando se inicia un conjunto de comandos de navegación de DVD.
ms.assetid: 9cdcb211-a9e3-4a15-81bd-7ada2b9d823a
title: EC_DVD_BeginNavigationCommands (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BeginNavigationCommands
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: cda904c4fcc0b1acdd16c8fc4596eef332140ec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680854"
---
# <a name="ec_dvd_beginnavigationcommands"></a><span data-ttu-id="84b99-103">\_BeginNavigationCommands de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="84b99-103">EC\_DVD\_BeginNavigationCommands</span></span>

<span data-ttu-id="84b99-104">Se envía cuando se inicia un conjunto de comandos de navegación de DVD.</span><span class="sxs-lookup"><span data-stu-id="84b99-104">Sent when a set of DVD navigation commands are starting.</span></span>

## <a name="parameters"></a><span data-ttu-id="84b99-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84b99-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84b99-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="84b99-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="84b99-107">Un valor de la enumeración [**\_ NavCmdType de DVD**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) .</span><span class="sxs-lookup"><span data-stu-id="84b99-107">A value from the [**DVD\_NavCmdType**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="84b99-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="84b99-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="84b99-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="84b99-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84b99-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84b99-110">Remarks</span></span>

<span data-ttu-id="84b99-111">Este evento está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="84b99-111">This event is disabled by default.</span></span> <span data-ttu-id="84b99-112">Para habilitar este evento, llame a [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **DVD \_ EnableLoggingEvents** en **true**.</span><span class="sxs-lookup"><span data-stu-id="84b99-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="84b99-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84b99-113">Requirements</span></span>



| <span data-ttu-id="84b99-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="84b99-114">Requirement</span></span> | <span data-ttu-id="84b99-115">Value</span><span class="sxs-lookup"><span data-stu-id="84b99-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b99-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84b99-116">Header</span></span><br/> | <dl> <span data-ttu-id="84b99-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84b99-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84b99-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="84b99-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b99-119">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="84b99-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="84b99-120">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="84b99-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="84b99-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="84b99-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




