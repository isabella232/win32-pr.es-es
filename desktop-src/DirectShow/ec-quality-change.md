---
description: El gráfico está quitando ejemplos para el control de calidad.
ms.assetid: a21fe766-58a5-4851-a282-883374287e18
title: EC_QUALITY_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5752db30c8ad6ed85655948cf2adb9ef7ac8078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678912"
---
# <a name="ec_quality_change"></a><span data-ttu-id="ee683-103">\_cambio de calidad de EC \_</span><span class="sxs-lookup"><span data-stu-id="ee683-103">EC\_QUALITY\_CHANGE</span></span>

<span data-ttu-id="ee683-104">El gráfico está quitando ejemplos para el control de calidad.</span><span class="sxs-lookup"><span data-stu-id="ee683-104">The graph is dropping samples, for quality control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee683-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee683-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee683-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ee683-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ee683-107">Cero.</span><span class="sxs-lookup"><span data-stu-id="ee683-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="ee683-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ee683-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ee683-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="ee683-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ee683-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="ee683-110">Default Action</span></span>

<span data-ttu-id="ee683-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ee683-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee683-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee683-112">Remarks</span></span>

<span data-ttu-id="ee683-113">Un filtro envía este evento si quita ejemplos en respuesta a un mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="ee683-113">A filter sends this event if it drops samples in response to a quality control message.</span></span> <span data-ttu-id="ee683-114">Envía el evento solo cuando ajusta el nivel de calidad, no para cada ejemplo que cae.</span><span class="sxs-lookup"><span data-stu-id="ee683-114">It sends the event only when it adjusts the quality level, not for each sample that it drops.</span></span> <span data-ttu-id="ee683-115">Para obtener más información, vea [Administración de control de calidad](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="ee683-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee683-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee683-116">Requirements</span></span>



| <span data-ttu-id="ee683-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee683-117">Requirement</span></span> | <span data-ttu-id="ee683-118">Value</span><span class="sxs-lookup"><span data-stu-id="ee683-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee683-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee683-119">Header</span></span><br/> | <dl> <span data-ttu-id="ee683-120"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee683-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee683-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee683-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee683-122">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="ee683-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ee683-123">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="ee683-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




