---
description: Indica el nuevo dominio del reproductor de DVD.
ms.assetid: 4faa46d6-2ba2-44a3-b237-acac3b32f8b1
title: EC_DVD_DOMAIN_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DOMAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 815b6b2dd318d0b7716f4cf640ef3f83dacd0d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653500"
---
# <a name="ec_dvd_domain_change"></a><span data-ttu-id="0abe3-103">\_cambio de \_ dominio de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="0abe3-103">EC\_DVD\_DOMAIN\_CHANGE</span></span>

<span data-ttu-id="0abe3-104">Indica el nuevo dominio del reproductor de DVD.</span><span class="sxs-lookup"><span data-stu-id="0abe3-104">Indicates the DVD player's new domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="0abe3-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0abe3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0abe3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0abe3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0abe3-107">Valor **DWORD** que indica el nuevo dominio.</span><span class="sxs-lookup"><span data-stu-id="0abe3-107">**DWORD** value indicating the new domain.</span></span> <span data-ttu-id="0abe3-108">Miembro del tipo de datos enumerado del [**\_ dominio de DVD**](/windows/win32/api/strmif/ne-strmif-dvd_domain) .</span><span class="sxs-lookup"><span data-stu-id="0abe3-108">Member of the [**DVD\_DOMAIN**](/windows/win32/api/strmif/ne-strmif-dvd_domain) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="0abe3-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0abe3-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0abe3-110">Cero.</span><span class="sxs-lookup"><span data-stu-id="0abe3-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0abe3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0abe3-111">Remarks</span></span>

<span data-ttu-id="0abe3-112">El reproductor de DVD indica este evento cada vez que cambia de dominio.</span><span class="sxs-lookup"><span data-stu-id="0abe3-112">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="0abe3-113">Este evento se desencadena en todos los dominios de DVD.</span><span class="sxs-lookup"><span data-stu-id="0abe3-113">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="0abe3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0abe3-114">Requirements</span></span>



| <span data-ttu-id="0abe3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0abe3-115">Requirement</span></span> | <span data-ttu-id="0abe3-116">Value</span><span class="sxs-lookup"><span data-stu-id="0abe3-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0abe3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0abe3-117">Header</span></span><br/> | <dl> <span data-ttu-id="0abe3-118"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0abe3-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0abe3-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0abe3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abe3-120">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="0abe3-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="0abe3-121">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="0abe3-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0abe3-122">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="0abe3-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




