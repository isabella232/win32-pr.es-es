---
description: Indica que se ha insertado un disco DVD en la unidad.
ms.assetid: ce233c94-2eae-457c-919b-7c4d8334979a
title: EC_DVD_DISC_INSERTED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_INSERTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c98d32960e2ab6a21633899164b3ff84525f2aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679477"
---
# <a name="ec_dvd_disc_inserted"></a><span data-ttu-id="2d5e1-103">\_disco DVD de EC \_ \_ insertado</span><span class="sxs-lookup"><span data-stu-id="2d5e1-103">EC\_DVD\_DISC\_INSERTED</span></span>

<span data-ttu-id="2d5e1-104">Indica que se ha insertado un disco DVD en la unidad.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-104">Signals that a DVD disc was inserted into the drive.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d5e1-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d5e1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d5e1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2d5e1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2d5e1-107">Cero.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="2d5e1-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2d5e1-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2d5e1-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d5e1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d5e1-110">Remarks</span></span>

<span data-ttu-id="2d5e1-111">La reproducción se inicia automáticamente cuando se inserta un disco.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-111">Playback automatically begins when a disc is inserted.</span></span> <span data-ttu-id="2d5e1-112">La aplicación no tiene que realizar ninguna acción especial en respuesta a este evento.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="2d5e1-113">Este evento se desencadena en todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d5e1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d5e1-114">Requirements</span></span>



| <span data-ttu-id="2d5e1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d5e1-115">Requirement</span></span> | <span data-ttu-id="2d5e1-116">Value</span><span class="sxs-lookup"><span data-stu-id="2d5e1-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5e1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d5e1-117">Header</span></span><br/> | <dl> <span data-ttu-id="2d5e1-118"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d5e1-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d5e1-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d5e1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d5e1-120">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="2d5e1-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="2d5e1-121">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="2d5e1-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2d5e1-122">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="2d5e1-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




