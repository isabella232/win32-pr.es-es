---
description: El modo de presentación ha cambiado.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549a4c5201906b692a1bd726e65269679705e9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680809"
---
# <a name="ec_display_changed"></a><span data-ttu-id="fc29a-103">visualización de EC \_ \_ modificada</span><span class="sxs-lookup"><span data-stu-id="fc29a-103">EC\_DISPLAY\_CHANGED</span></span>

<span data-ttu-id="fc29a-104">El modo de presentación ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fc29a-104">The display mode has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc29a-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc29a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc29a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="fc29a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="fc29a-107">(**IUnknown** \* ) Puntero a una matriz de interfaces [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) para los pines de entrada del representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc29a-107">(**IUnknown**\*) Pointer to an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces for the video renderer's input pins.</span></span> <span data-ttu-id="fc29a-108">Si *lParam2* es cero, este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="fc29a-108">If *lParam2* is zero, this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fc29a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="fc29a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="fc29a-110">Si *lParam2* es cero, *lParam1* contiene un único puntero **IPin** o es igual a **null**.</span><span class="sxs-lookup"><span data-stu-id="fc29a-110">If *lParam2* is zero, *lParam1* contains a single **IPin** pointer or equals **NULL**.</span></span> <span data-ttu-id="fc29a-111">Si *lParam2* es mayor que cero, *lParam1* contiene una matriz de punteros **IPin** y el número de elementos de la matriz lo proporciona *lParam2*.</span><span class="sxs-lookup"><span data-stu-id="fc29a-111">If *lParam2* is greater than zero, *lParam1* contains an array of **IPin** pointers, and the number of elements in the array is given by *lParam2*.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="fc29a-112">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="fc29a-112">Default Action</span></span>

<span data-ttu-id="fc29a-113">El administrador de gráficos de filtro detiene temporalmente el gráfico y, a continuación, desconecta y vuelve a conectar el representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc29a-113">The filter graph manager temporarily stops the graph, and then disconnects and reconnects the video renderer.</span></span> <span data-ttu-id="fc29a-114">No pasa el evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc29a-114">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc29a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc29a-115">Remarks</span></span>

<span data-ttu-id="fc29a-116">Los representadores de vídeo pueden enviar este evento en respuesta a un mensaje de [**\_ DISPLAYCHANGE de WM**](/windows/desktop/gdi/wm-displaychange) .</span><span class="sxs-lookup"><span data-stu-id="fc29a-116">Video renderers can send this event in response to a [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span> <span data-ttu-id="fc29a-117">El mensaje de **\_ DISPLAYCHANGE de WM** indica que el usuario ha cambiado la resolución de pantalla.</span><span class="sxs-lookup"><span data-stu-id="fc29a-117">The **WM\_DISPLAYCHANGE** message indicates that the user has changed the display resolution.</span></span>

<span data-ttu-id="fc29a-118">Durante la conexión de PIN, la mayoría de los representadores de vídeo eligen un formato basado en el modo de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="fc29a-118">During pin connection, most video renderers pick a format based on the current display mode.</span></span> <span data-ttu-id="fc29a-119">Si cambia el modo de presentación, es posible que el representador de vídeo tenga que elegir otro formato.</span><span class="sxs-lookup"><span data-stu-id="fc29a-119">If the display mode changes, the video renderer might need to choose another format.</span></span> <span data-ttu-id="fc29a-120">Al enviar este mensaje, el representador señala al administrador de gráficos de filtro que debe volver a conectarse.</span><span class="sxs-lookup"><span data-stu-id="fc29a-120">By sending this message, the renderer signals to the filter graph manager that it needs to be reconnected.</span></span> <span data-ttu-id="fc29a-121">Durante la reconexión, el representador puede seleccionar un nuevo formato.</span><span class="sxs-lookup"><span data-stu-id="fc29a-121">During the reconnection, the renderer can select a new format.</span></span> <span data-ttu-id="fc29a-122">Si se produce un error en la reconexión, el administrador de gráficos de filtros envía un evento [**\_ ERRORABORT de EC**](ec-errorabort.md) a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc29a-122">If the reconnection fails, the filter graph manager sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the application.</span></span>

### <a name="enhanced-video-renderer"></a><span data-ttu-id="fc29a-123">Representador de vídeo mejorado</span><span class="sxs-lookup"><span data-stu-id="fc29a-123">Enhanced Video Renderer</span></span>

<span data-ttu-id="fc29a-124">Un presentador personalizado para el [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR) debe enviar este evento a evr si cambia el dispositivo Direct3D del presentador.</span><span class="sxs-lookup"><span data-stu-id="fc29a-124">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) should send this event to the EVR if the presenter's Direct3D device changes.</span></span> <span data-ttu-id="fc29a-125">Establezca *lParam1* y *lParam2* en cero; EVR omite los parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="fc29a-125">Set *lParam1* and *lParam2* to zero; the EVR ignores the event parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc29a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc29a-126">Requirements</span></span>



| <span data-ttu-id="fc29a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc29a-127">Requirement</span></span> | <span data-ttu-id="fc29a-128">Value</span><span class="sxs-lookup"><span data-stu-id="fc29a-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc29a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc29a-129">Header</span></span><br/> | <dl> <span data-ttu-id="fc29a-130"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc29a-130"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc29a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc29a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc29a-132">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="fc29a-132">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="fc29a-133">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="fc29a-133">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

