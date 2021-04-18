---
description: Se envía cuando el navegador de DVD procesa un comando de navegación por DVD.
ms.assetid: 95e502b6-330f-4bc7-8adc-851913987370
title: EC_DVD_NavigationCommand (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_NavigationCommand
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e81dbf108868cbaec4c44a436f2c8271bb5f282a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653498"
---
# <a name="ec_dvd_navigationcommand"></a><span data-ttu-id="d68b0-103">\_NavigationCommand de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="d68b0-103">EC\_DVD\_NavigationCommand</span></span>

<span data-ttu-id="d68b0-104">Se envía cuando el [navegador de DVD](dvd-navigator-filter.md) procesa un comando de navegación por DVD.</span><span class="sxs-lookup"><span data-stu-id="d68b0-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) processes a DVD navigation command.</span></span>

## <a name="parameters"></a><span data-ttu-id="d68b0-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d68b0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d68b0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d68b0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d68b0-107">Los 32 bits inferiores del comando de navegación sin formato.</span><span class="sxs-lookup"><span data-stu-id="d68b0-107">The lower 32 bits of the raw navigation command.</span></span>

</dd> <dt>

<span data-ttu-id="d68b0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d68b0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d68b0-109">Los 32 bits superiores del comando de navegación sin formato.</span><span class="sxs-lookup"><span data-stu-id="d68b0-109">The upper 32 bits of the raw navigation command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d68b0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d68b0-110">Remarks</span></span>

<span data-ttu-id="d68b0-111">Este evento está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d68b0-111">This event is disabled by default.</span></span> <span data-ttu-id="d68b0-112">Para habilitar este evento, llame a [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **DVD \_ EnableLoggingEvents** en **true**.</span><span class="sxs-lookup"><span data-stu-id="d68b0-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d68b0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d68b0-113">Requirements</span></span>



| <span data-ttu-id="d68b0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d68b0-114">Requirement</span></span> | <span data-ttu-id="d68b0-115">Value</span><span class="sxs-lookup"><span data-stu-id="d68b0-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d68b0-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d68b0-116">Header</span></span><br/> | <dl> <span data-ttu-id="d68b0-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d68b0-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d68b0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d68b0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d68b0-119">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="d68b0-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="d68b0-120">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="d68b0-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d68b0-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d68b0-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




