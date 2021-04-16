---
description: El representador de vídeo se ha destruido o quitado del gráfico.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679127"
---
# <a name="ec_window_destroyed"></a><span data-ttu-id="16996-103">ventana de EC \_ \_ destruida</span><span class="sxs-lookup"><span data-stu-id="16996-103">EC\_WINDOW\_DESTROYED</span></span>

<span data-ttu-id="16996-104">El representador de vídeo se ha destruido o quitado del gráfico.</span><span class="sxs-lookup"><span data-stu-id="16996-104">The video renderer was destroyed or removed from the graph.</span></span>

## <a name="parameters"></a><span data-ttu-id="16996-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16996-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16996-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="16996-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="16996-107">(**IUnknown** \* ) Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="16996-107">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> <dt>

<span data-ttu-id="16996-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="16996-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="16996-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="16996-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="16996-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="16996-110">Default Action</span></span>

<span data-ttu-id="16996-111">El administrador de gráficos de filtros libera esta ventana como el foco, a través de la interfaz [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="16996-111">The filter graph manager releases this window as the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="16996-112">No envía la notificación de eventos a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="16996-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="16996-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16996-113">Remarks</span></span>

<span data-ttu-id="16996-114">El representador de vídeo envía este evento cuando sale del gráfico de filtros, en el método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .</span><span class="sxs-lookup"><span data-stu-id="16996-114">The video renderer sends this event when it leaves the filter graph, in its [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="16996-115">(El envío del evento cuando se destruye el filtro puede ser demasiado tarde, porque en ese momento también podría destruirse el administrador de gráficos de filtros).</span><span class="sxs-lookup"><span data-stu-id="16996-115">(Sending the event when the filter is destroyed might be too late, because at that point the filter graph manager might also be destroyed.)</span></span>

<span data-ttu-id="16996-116">Este evento permite que otros filtros adquieran recursos que dependen del foco de la ventana, como dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="16996-116">This event enables other filters to acquire resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="16996-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16996-117">Requirements</span></span>



| <span data-ttu-id="16996-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="16996-118">Requirement</span></span> | <span data-ttu-id="16996-119">Value</span><span class="sxs-lookup"><span data-stu-id="16996-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16996-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16996-120">Header</span></span><br/> | <dl> <span data-ttu-id="16996-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="16996-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16996-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="16996-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16996-123">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="16996-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="16996-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="16996-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




