---
description: Se envía cuando cambia el número de programa o el número de celda del DVD.
ms.assetid: a500e86d-cd42-4716-9c57-828a72c4e1df
title: EC_DVD_PROGRAM_CELL_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CELL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: d41f691016c3e41cfc3e14ed1ce6fff276dcc70e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653406"
---
# <a name="ec_dvd_program_cell_change"></a><span data-ttu-id="cb10b-103">\_cambio de \_ celda del programa de DVD de EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="cb10b-103">EC\_DVD\_PROGRAM\_CELL\_CHANGE</span></span>

<span data-ttu-id="cb10b-104">Se envía cuando cambia el número de programa o el número de celda del DVD.</span><span class="sxs-lookup"><span data-stu-id="cb10b-104">Sent when the DVD program number or cell number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb10b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb10b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb10b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="cb10b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cb10b-107">El nuevo número de programa.</span><span class="sxs-lookup"><span data-stu-id="cb10b-107">The new program number.</span></span>

</dd> <dt>

<span data-ttu-id="cb10b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cb10b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cb10b-109">El nuevo número de celda.</span><span class="sxs-lookup"><span data-stu-id="cb10b-109">The new cell number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb10b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb10b-110">Remarks</span></span>

<span data-ttu-id="cb10b-111">Este evento está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cb10b-111">This event is disabled by default.</span></span> <span data-ttu-id="cb10b-112">Para habilitar este evento, llame a [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **DVD \_ NotifyPositionChange** en **true**.</span><span class="sxs-lookup"><span data-stu-id="cb10b-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb10b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb10b-113">Requirements</span></span>



| <span data-ttu-id="cb10b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb10b-114">Requirement</span></span> | <span data-ttu-id="cb10b-115">Value</span><span class="sxs-lookup"><span data-stu-id="cb10b-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb10b-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb10b-116">Header</span></span><br/> | <dl> <span data-ttu-id="cb10b-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb10b-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb10b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb10b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb10b-119">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="cb10b-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="cb10b-120">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="cb10b-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="cb10b-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="cb10b-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




