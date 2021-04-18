---
description: Un filtro no recibe suficientes datos.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653356"
---
# <a name="ec_starvation"></a><span data-ttu-id="ca87d-103">colapso de EC \_</span><span class="sxs-lookup"><span data-stu-id="ca87d-103">EC\_STARVATION</span></span>

<span data-ttu-id="ca87d-104">Un filtro no recibe suficientes datos.</span><span class="sxs-lookup"><span data-stu-id="ca87d-104">A filter is not receiving enough data.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca87d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca87d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca87d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ca87d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ca87d-107">Cero.</span><span class="sxs-lookup"><span data-stu-id="ca87d-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="ca87d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ca87d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ca87d-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="ca87d-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ca87d-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="ca87d-110">Default Action</span></span>

<span data-ttu-id="ca87d-111">El evento no se envía a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ca87d-111">The event is not sent to the application.</span></span> <span data-ttu-id="ca87d-112">Si el gráfico de filtros se está ejecutando, el administrador de gráficos de filtro pausa el gráfico y espera a que se complete la pausa.</span><span class="sxs-lookup"><span data-stu-id="ca87d-112">If the filter graph is running, the filter graph manager pauses the graph and waits for the pause to complete.</span></span> <span data-ttu-id="ca87d-113">A continuación, vuelve a ejecutar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="ca87d-113">Then it runs the graph again.</span></span> <span data-ttu-id="ca87d-114">El filtro que envía el evento no debe completar su transición a pausado hasta que tenga suficientes datos para reanudar.</span><span class="sxs-lookup"><span data-stu-id="ca87d-114">The filter sending the event should not complete its transition to paused until it has enough data to resume.</span></span> <span data-ttu-id="ca87d-115">Si el gráfico de filtros no se está ejecutando, el administrador de gráficos de filtro omite este evento.</span><span class="sxs-lookup"><span data-stu-id="ca87d-115">If the filter graph is not running, the filter graph manager ignores this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca87d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca87d-116">Remarks</span></span>

<span data-ttu-id="ca87d-117">Un analizador o filtro de origen puede enviar este evento si llegan demasiado pocos datos.</span><span class="sxs-lookup"><span data-stu-id="ca87d-117">A parser or source filter can send this event if too little data is arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca87d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca87d-118">Requirements</span></span>



| <span data-ttu-id="ca87d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca87d-119">Requirement</span></span> | <span data-ttu-id="ca87d-120">Value</span><span class="sxs-lookup"><span data-stu-id="ca87d-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca87d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca87d-121">Header</span></span><br/> | <dl> <span data-ttu-id="ca87d-122"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca87d-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca87d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca87d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca87d-124">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="ca87d-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ca87d-125">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="ca87d-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




