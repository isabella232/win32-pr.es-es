---
description: Indica que se ha iniciado un cambio de frecuencia en la reproducción de DVD.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 20ddc41fd70906fabc522daa4dcb7714b71e4251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679349"
---
# <a name="ec_dvd_playback_rate_change"></a><span data-ttu-id="7201c-103">\_cambio de \_ velocidad de reproducción de DVD de EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="7201c-103">EC\_DVD\_PLAYBACK\_RATE\_CHANGE</span></span>

<span data-ttu-id="7201c-104">Indica que se ha iniciado un cambio de frecuencia en la reproducción de DVD.</span><span class="sxs-lookup"><span data-stu-id="7201c-104">Signals that a rate change in DVD playback has been initiated.</span></span>

## <a name="parameters"></a><span data-ttu-id="7201c-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7201c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7201c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7201c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7201c-107">LARGO que indica la velocidad de reproducción nueva.</span><span class="sxs-lookup"><span data-stu-id="7201c-107">LONG indicating the new playback rate.</span></span> <span data-ttu-id="7201c-108">El valor es la velocidad de reproducción real multiplicada por 10.000, por lo que la velocidad de reproducción es igual a 10000,0/ *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="7201c-108">The value is the actual playback rate multiplied by 10,000, so the playback rate equals 10000.0 / *lParam1*.</span></span> <span data-ttu-id="7201c-109">Los valores menores que cero indican el modo de reproducción inversa y los valores mayores que cero indican el modo de reproducción hacia delante.</span><span class="sxs-lookup"><span data-stu-id="7201c-109">Values less than zero indicate reverse playback mode, and values greater than zero indicate forward playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="7201c-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7201c-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7201c-111">Cero.</span><span class="sxs-lookup"><span data-stu-id="7201c-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7201c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7201c-112">Remarks</span></span>

<span data-ttu-id="7201c-113">Este evento se desencadena en el dominio de título.</span><span class="sxs-lookup"><span data-stu-id="7201c-113">This event is raised in the title domain.</span></span>

<span data-ttu-id="7201c-114">La *velocidad de reproducción es el* inverso de la *velocidad* de reproducción.</span><span class="sxs-lookup"><span data-stu-id="7201c-114">Playback *rate* is the inverse of playback *speed*.</span></span> <span data-ttu-id="7201c-115">Por ejemplo, si la velocidad de reproducción es 2x, la velocidad es 0,5.</span><span class="sxs-lookup"><span data-stu-id="7201c-115">For example, if playback speed is 2x, the rate is 0.5.</span></span>

## <a name="requirements"></a><span data-ttu-id="7201c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7201c-116">Requirements</span></span>



| <span data-ttu-id="7201c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7201c-117">Requirement</span></span> | <span data-ttu-id="7201c-118">Value</span><span class="sxs-lookup"><span data-stu-id="7201c-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7201c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7201c-119">Header</span></span><br/> | <dl> <span data-ttu-id="7201c-120"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7201c-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7201c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7201c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7201c-122">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="7201c-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7201c-123">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="7201c-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7201c-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="7201c-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




