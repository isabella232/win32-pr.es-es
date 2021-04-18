---
description: Indica que el navegador ha terminado de reproducirse el segmento especificado en una llamada a IDvdControl2::P layPeriodInTitleAutoStop.
ms.assetid: 1716eabe-f106-436a-8a6a-ca43cee9341c
title: EC_DVD_PLAYPERIOD_AUTOSTOP (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYPERIOD_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c2081c8a5b7e5b6bd2165781af9552722ed9ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679348"
---
# <a name="ec_dvd_playperiod_autostop"></a><span data-ttu-id="56f7f-103">\_detención de \_ PLAYPERIOD de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="56f7f-103">EC\_DVD\_PLAYPERIOD\_AUTOSTOP</span></span>

<span data-ttu-id="56f7f-104">Indica que el navegador ha terminado de reproducirse el segmento especificado en una llamada a [**IDvdControl2::P layperiodintitleautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop).</span><span class="sxs-lookup"><span data-stu-id="56f7f-104">Indicates that the Navigator has finished playing the segment specified in a call to [**IDvdControl2::PlayPeriodInTitleAutoStop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop).</span></span>

## <a name="parameters"></a><span data-ttu-id="56f7f-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56f7f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56f7f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="56f7f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="56f7f-107">Cero.</span><span class="sxs-lookup"><span data-stu-id="56f7f-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="56f7f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="56f7f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="56f7f-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="56f7f-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56f7f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56f7f-110">Remarks</span></span>

<span data-ttu-id="56f7f-111">Este evento se desencadena en el dominio de título.</span><span class="sxs-lookup"><span data-stu-id="56f7f-111">This event is raised in the Title domain.</span></span>

<span data-ttu-id="56f7f-112">Este evento también se envía cuando se cancela la reproducción antes de que el navegador finalice la reproducción del segmento especificado.</span><span class="sxs-lookup"><span data-stu-id="56f7f-112">This event is also sent when playback is canceled before the Navigator finishes playing the specified segment.</span></span>

## <a name="requirements"></a><span data-ttu-id="56f7f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56f7f-113">Requirements</span></span>



| <span data-ttu-id="56f7f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="56f7f-114">Requirement</span></span> | <span data-ttu-id="56f7f-115">Value</span><span class="sxs-lookup"><span data-stu-id="56f7f-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56f7f-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56f7f-116">Header</span></span><br/> | <dl> <span data-ttu-id="56f7f-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56f7f-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56f7f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="56f7f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56f7f-119">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="56f7f-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="56f7f-120">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="56f7f-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="56f7f-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="56f7f-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="56f7f-122">**IDvdControl2::P layPeriodInTitleAutoStop**</span><span class="sxs-lookup"><span data-stu-id="56f7f-122">**IDvdControl2::PlayPeriodInTitleAutoStop**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)
</dt> </dl>

 

 




