---
description: El representador de vídeo está cambiando del modo de pantalla completa.
ms.assetid: f720a9b6-930a-4ed7-9798-1c72fa7a11ff
title: EC_FULLSCREEN_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf36b5652ea5f7cde26950a18de086af0862dac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680312"
---
# <a name="ec_fullscreen_lost"></a><span data-ttu-id="73199-103">\_pantalla completa de EC \_ perdida</span><span class="sxs-lookup"><span data-stu-id="73199-103">EC\_FULLSCREEN\_LOST</span></span>

<span data-ttu-id="73199-104">El representador de vídeo está cambiando del modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="73199-104">The video renderer is switching out of full-screen mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="73199-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73199-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73199-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="73199-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="73199-107">Cero.</span><span class="sxs-lookup"><span data-stu-id="73199-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="73199-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="73199-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="73199-109">(**IUnknown** \* ) Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del representador de vídeo, o **null**.</span><span class="sxs-lookup"><span data-stu-id="73199-109">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="73199-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="73199-110">Default Action</span></span>

<span data-ttu-id="73199-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="73199-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="73199-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73199-112">Remarks</span></span>

<span data-ttu-id="73199-113">Cuando el [representador de pantalla completa](full-screen-renderer-filter.md) pierde la activación, envía este evento.</span><span class="sxs-lookup"><span data-stu-id="73199-113">When the [Full Screen Renderer](full-screen-renderer-filter.md) loses activation, it sends this event.</span></span> <span data-ttu-id="73199-114">Cuando otro representador de vídeo cambia de modo de pantalla completa, el administrador de gráficos de filtros envía este evento, en respuesta a un evento de [**\_ activación de EC**](ec-activate.md) del representador.</span><span class="sxs-lookup"><span data-stu-id="73199-114">When another video renderer switches out of full-screen mode, the filter graph manager sends this event, in response to an [**EC\_ACTIVATE**](ec-activate.md) event from the renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="73199-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73199-115">Requirements</span></span>



| <span data-ttu-id="73199-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="73199-116">Requirement</span></span> | <span data-ttu-id="73199-117">Value</span><span class="sxs-lookup"><span data-stu-id="73199-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73199-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73199-118">Header</span></span><br/> | <dl> <span data-ttu-id="73199-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="73199-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73199-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="73199-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73199-121">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="73199-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="73199-122">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="73199-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




