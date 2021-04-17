---
description: Indica que se ha detenido la reproducción de DVD. Este evento se envía cuando se completa un título o un capítulo y el navegador de DVD no encuentra ninguna otra instrucción de bifurcación para la posterior reproducción. El evento no se envía cuando la aplicación detiene la reproducción.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2304d83aea532b764777b683c57c3bdd4d5df79a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653495"
---
# <a name="ec_dvd_playback_stopped"></a><span data-ttu-id="a880a-105">reproducción de DVD de EC \_ \_ \_ detenida</span><span class="sxs-lookup"><span data-stu-id="a880a-105">EC\_DVD\_PLAYBACK\_STOPPED</span></span>

<span data-ttu-id="a880a-106">Indica que se ha detenido la reproducción de DVD.</span><span class="sxs-lookup"><span data-stu-id="a880a-106">Indicates that DVD playback has been stopped.</span></span> <span data-ttu-id="a880a-107">Este evento se envía cuando se completa un título o un capítulo y el [navegador de DVD](dvd-navigator-filter.md) no encuentra ninguna otra instrucción de bifurcación para la posterior reproducción.</span><span class="sxs-lookup"><span data-stu-id="a880a-107">This event is sent when a title or chapter completes and the [DVD Navigator](dvd-navigator-filter.md) does not find any other branching instruction for subsequent playback.</span></span> <span data-ttu-id="a880a-108">El evento no se envía cuando la aplicación detiene la reproducción.</span><span class="sxs-lookup"><span data-stu-id="a880a-108">The event is not sent when the application stops playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="a880a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a880a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a880a-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a880a-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a880a-111">Un miembro de la enumeración [**\_ \_ Stopped de DVD PB**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) , que indica por qué se detuvo la reproducción.</span><span class="sxs-lookup"><span data-stu-id="a880a-111">A member of the [**DVD\_PB\_STOPPED**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) enumeration, indicating why playback stopped.</span></span>

</dd> <dt>

<span data-ttu-id="a880a-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a880a-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a880a-113">Cero.</span><span class="sxs-lookup"><span data-stu-id="a880a-113">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a880a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a880a-114">Remarks</span></span>

<span data-ttu-id="a880a-115">Este evento se desencadena en todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="a880a-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="a880a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a880a-116">Requirements</span></span>



| <span data-ttu-id="a880a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a880a-117">Requirement</span></span> | <span data-ttu-id="a880a-118">Value</span><span class="sxs-lookup"><span data-stu-id="a880a-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a880a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a880a-119">Header</span></span><br/> | <dl> <span data-ttu-id="a880a-120"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a880a-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a880a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a880a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a880a-122">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="a880a-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="a880a-123">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="a880a-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a880a-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="a880a-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




