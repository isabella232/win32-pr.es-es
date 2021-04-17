---
description: Notifica a un filtro la ventana del representador de vídeo.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680988"
---
# <a name="ec_notify_window"></a><span data-ttu-id="e4102-103">\_ventana notificación de EC \_</span><span class="sxs-lookup"><span data-stu-id="e4102-103">EC\_NOTIFY\_WINDOW</span></span>

<span data-ttu-id="e4102-104">Notifica a un filtro la ventana del representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e4102-104">Notifies a filter of the video renderer's window.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4102-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4102-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4102-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e4102-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e4102-107">(**HWnd**) Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="e4102-107">(**HWND**) Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="e4102-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e4102-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e4102-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="e4102-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="e4102-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="e4102-110">Default Action</span></span>

<span data-ttu-id="e4102-111">DirectShow usa internamente este evento.</span><span class="sxs-lookup"><span data-stu-id="e4102-111">This event is used internally by DirectShow.</span></span> <span data-ttu-id="e4102-112">El administrador de gráficos de filtro no pasa este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e4102-112">The filter graph manager does not pass this event to the application.</span></span> <span data-ttu-id="e4102-113">Las aplicaciones no pueden invalidar la acción predeterminada para este evento.</span><span class="sxs-lookup"><span data-stu-id="e4102-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4102-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4102-114">Remarks</span></span>

<span data-ttu-id="e4102-115">Cuando se conecta un representador de vídeo, comprueba si el PIN de salida ascendente admite la interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="e4102-115">When a video renderer is connected, it checks whether the upstream output pin supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="e4102-116">Si es así, el representador envía este evento al filtro de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="e4102-116">If so, the renderer sends this event to the upstream filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4102-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4102-117">Requirements</span></span>



| <span data-ttu-id="e4102-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4102-118">Requirement</span></span> | <span data-ttu-id="e4102-119">Value</span><span class="sxs-lookup"><span data-stu-id="e4102-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4102-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4102-120">Header</span></span><br/> | <dl> <span data-ttu-id="e4102-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4102-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4102-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4102-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4102-123">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="e4102-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e4102-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="e4102-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




