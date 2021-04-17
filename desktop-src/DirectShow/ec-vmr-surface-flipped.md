---
description: Se envía cuando el presentador del asignador VMR-7's ha llamado al método Flip de DirectDraw en la superficie que se está presentando. Esto permite que VMR mantenga su tabla de superficies DirectXVA sincronizada con la cadena de volteo de DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653755"
---
# <a name="ec_vmr_surface_flipped"></a><span data-ttu-id="548ca-104">\_superficie EC \_ VMR \_ volteada</span><span class="sxs-lookup"><span data-stu-id="548ca-104">EC\_VMR\_SURFACE\_FLIPPED</span></span>

<span data-ttu-id="548ca-105">Se envía cuando el presentador del asignador VMR-7's ha llamado al método Flip de DirectDraw en la superficie que se está presentando.</span><span class="sxs-lookup"><span data-stu-id="548ca-105">Sent when the VMR-7's allocator presenter has called the DirectDraw Flip method on the surface being presented.</span></span> <span data-ttu-id="548ca-106">Esto permite que VMR mantenga su tabla de superficies DirectXVA sincronizada con la cadena de volteo de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="548ca-106">This allows the VMR to keep its DirectXVA table of surfaces synchronized with DirectDraw's flipping chain.</span></span>

## <a name="parameters"></a><span data-ttu-id="548ca-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="548ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="548ca-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="548ca-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="548ca-109">(**HRESULT**) Código de estado devuelto por el método DirectDraw flip.</span><span class="sxs-lookup"><span data-stu-id="548ca-109">(**HRESULT**) Status code returned from the DirectDraw Flip method.</span></span>

</dd> <dt>

<span data-ttu-id="548ca-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="548ca-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="548ca-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="548ca-111">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="548ca-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="548ca-112">Remarks</span></span>

<span data-ttu-id="548ca-113">Asignador personalizado: los presentadores de VMR-7 deben enviar este evento.</span><span class="sxs-lookup"><span data-stu-id="548ca-113">Custom allocator-presenters for the VMR-7 should send this event.</span></span> <span data-ttu-id="548ca-114">Este evento no se reenvía a las aplicaciones y no se usa con los presentadores de asignador para VMR-9.</span><span class="sxs-lookup"><span data-stu-id="548ca-114">This event is not forwarded to applications and it is not used with allocator-presenters for the VMR-9.</span></span>

## <a name="requirements"></a><span data-ttu-id="548ca-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="548ca-115">Requirements</span></span>



| <span data-ttu-id="548ca-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="548ca-116">Requirement</span></span> | <span data-ttu-id="548ca-117">Value</span><span class="sxs-lookup"><span data-stu-id="548ca-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="548ca-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="548ca-118">Header</span></span><br/> | <dl> <span data-ttu-id="548ca-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="548ca-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="548ca-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="548ca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="548ca-121">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="548ca-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="548ca-122">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="548ca-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




