---
description: El usuario ha terminado la reproducción.
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: EC_USERABORT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680235"
---
# <a name="ec_userabort"></a><span data-ttu-id="824d5-103">USERABORT de EC \_</span><span class="sxs-lookup"><span data-stu-id="824d5-103">EC\_USERABORT</span></span>

<span data-ttu-id="824d5-104">El usuario ha terminado la reproducción.</span><span class="sxs-lookup"><span data-stu-id="824d5-104">The user has terminated playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="824d5-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="824d5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="824d5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="824d5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="824d5-107">Cero.</span><span class="sxs-lookup"><span data-stu-id="824d5-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="824d5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="824d5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="824d5-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="824d5-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="824d5-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="824d5-110">Default Action</span></span>

<span data-ttu-id="824d5-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="824d5-111">None.</span></span> <span data-ttu-id="824d5-112">La aplicación debe decidir si desea detener el gráfico.</span><span class="sxs-lookup"><span data-stu-id="824d5-112">The application must decide whether to stop the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="824d5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="824d5-113">Remarks</span></span>

<span data-ttu-id="824d5-114">Este código de evento indica que el usuario ha terminado la reproducción de gráficos normal.</span><span class="sxs-lookup"><span data-stu-id="824d5-114">This event code signals that the user has terminated normal graph playback.</span></span> <span data-ttu-id="824d5-115">Por ejemplo, los representadores de vídeo envían este evento si el usuario cierra la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="824d5-115">For example, video renderers send this event if the user closes the video window.</span></span>

<span data-ttu-id="824d5-116">Después de enviar este evento, el filtro debe rechazar todas las muestras y no enviar ningún evento [**\_ Repaint de EC**](ec-repaint.md) , hasta que el filtro se detenga y se restablezca.</span><span class="sxs-lookup"><span data-stu-id="824d5-116">After sending this event, the filter should reject all samples and not send any [**EC\_REPAINT**](ec-repaint.md) events, until the filter stops and is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="824d5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="824d5-117">Requirements</span></span>



| <span data-ttu-id="824d5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="824d5-118">Requirement</span></span> | <span data-ttu-id="824d5-119">Value</span><span class="sxs-lookup"><span data-stu-id="824d5-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="824d5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="824d5-120">Header</span></span><br/> | <dl> <span data-ttu-id="824d5-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="824d5-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="824d5-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="824d5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824d5-123">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="824d5-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="824d5-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="824d5-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




