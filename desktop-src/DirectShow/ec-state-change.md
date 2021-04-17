---
description: El gráfico de filtro ha cambiado de estado.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690323"
---
# <a name="ec_state_change"></a><span data-ttu-id="5ca3f-103">\_cambio de estado de EC \_</span><span class="sxs-lookup"><span data-stu-id="5ca3f-103">EC\_STATE\_CHANGE</span></span>

<span data-ttu-id="5ca3f-104">El gráfico de filtro ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="5ca3f-104">The filter graph has changed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ca3f-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ca3f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca3f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="5ca3f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="5ca3f-107">(**DWORD**) Miembro del tipo enumerado de [**\_ Estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , que indica el nuevo estado del gráfico.</span><span class="sxs-lookup"><span data-stu-id="5ca3f-107">(**DWORD**) Member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the new graph state.</span></span>

</dd> <dt>

<span data-ttu-id="5ca3f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="5ca3f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="5ca3f-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="5ca3f-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="5ca3f-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="5ca3f-110">Default Action</span></span>

<span data-ttu-id="5ca3f-111">Ninguna acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ca3f-111">No default action.</span></span> <span data-ttu-id="5ca3f-112">El evento no se envía a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ca3f-112">The event is not sent to the application.</span></span>

> [!Note]  
> <span data-ttu-id="5ca3f-113">Este evento puede producirse cuando se cierra el gráfico.</span><span class="sxs-lookup"><span data-stu-id="5ca3f-113">This event can occur when the graph shuts down.</span></span> <span data-ttu-id="5ca3f-114">Si invalida la acción predeterminada y escucha este evento, debe tener especial cuidado de no procesar eventos después de liberar el administrador de gráficos de filtros.</span><span class="sxs-lookup"><span data-stu-id="5ca3f-114">If you override the default action and listen for this event, you must be especially careful not to process events after releasing the Filter Graph Manager.</span></span> <span data-ttu-id="5ca3f-115">De lo contrario, la aplicación podría hacer referencia a un puntero [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) no válido y bloquearse.</span><span class="sxs-lookup"><span data-stu-id="5ca3f-115">Otherwise, your application might reference an invalid [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) pointer and crash.</span></span> <span data-ttu-id="5ca3f-116">Para obtener más información, consulte [responder a eventos](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="5ca3f-116">For more information, see [Responding to Events](responding-to-events.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ca3f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ca3f-117">Requirements</span></span>



| <span data-ttu-id="5ca3f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ca3f-118">Requirement</span></span> | <span data-ttu-id="5ca3f-119">Value</span><span class="sxs-lookup"><span data-stu-id="5ca3f-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca3f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ca3f-120">Header</span></span><br/> | <dl> <span data-ttu-id="5ca3f-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ca3f-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ca3f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ca3f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca3f-123">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="5ca3f-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="5ca3f-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="5ca3f-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




