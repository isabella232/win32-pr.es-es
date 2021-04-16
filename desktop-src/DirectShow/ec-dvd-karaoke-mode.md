---
description: Indica que el navegador de DVD ha empezado a reproducir o ha terminado de reproducir los datos de karaoke.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fb83bc1de9c2933b53935c056b192eca74c4245c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679357"
---
# <a name="ec_dvd_karaoke_mode"></a><span data-ttu-id="ee660-103">\_modo de \_ Karaoke de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="ee660-103">EC\_DVD\_KARAOKE\_MODE</span></span>

<span data-ttu-id="ee660-104">Indica que el [navegador de DVD](data-flow-in-the-dvd-navigator.md) ha empezado a reproducir o ha terminado de reproducir los datos de karaoke.</span><span class="sxs-lookup"><span data-stu-id="ee660-104">Indicates that the [DVD Navigator](data-flow-in-the-dvd-navigator.md) has either begun playing or finished playing karaoke data.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee660-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee660-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee660-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ee660-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ee660-107">Valor booleano.</span><span class="sxs-lookup"><span data-stu-id="ee660-107">Boolean value.</span></span> <span data-ttu-id="ee660-108">Si es **true**, se está reproduciendo una pista de karaoke.</span><span class="sxs-lookup"><span data-stu-id="ee660-108">If **TRUE**, a karaoke track is being played.</span></span> <span data-ttu-id="ee660-109">De lo contrario, no se está reproduciendo ninguna pista de karaoke.</span><span class="sxs-lookup"><span data-stu-id="ee660-109">Otherwise, no karaoke track is being played.</span></span>

</dd> <dt>

<span data-ttu-id="ee660-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ee660-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ee660-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ee660-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee660-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee660-112">Remarks</span></span>

<span data-ttu-id="ee660-113">El reproductor de DVD indica este evento cada vez que cambia de dominio.</span><span class="sxs-lookup"><span data-stu-id="ee660-113">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="ee660-114">Este evento se desencadena en todos los dominios de DVD.</span><span class="sxs-lookup"><span data-stu-id="ee660-114">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee660-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee660-115">Requirements</span></span>



| <span data-ttu-id="ee660-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee660-116">Requirement</span></span> | <span data-ttu-id="ee660-117">Value</span><span class="sxs-lookup"><span data-stu-id="ee660-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee660-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee660-118">Header</span></span><br/> | <dl> <span data-ttu-id="ee660-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee660-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee660-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee660-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee660-121">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="ee660-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="ee660-122">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="ee660-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ee660-123">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="ee660-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




