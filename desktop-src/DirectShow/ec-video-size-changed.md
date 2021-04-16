---
description: El tamaño de vídeo nativo ha cambiado.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680234"
---
# <a name="ec_video_size_changed"></a><span data-ttu-id="37fad-103">tamaño de vídeo de EC \_ \_ \_ cambiado</span><span class="sxs-lookup"><span data-stu-id="37fad-103">EC\_VIDEO\_SIZE\_CHANGED</span></span>

<span data-ttu-id="37fad-104">El tamaño de vídeo nativo ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="37fad-104">The native video size has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="37fad-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37fad-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37fad-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="37fad-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="37fad-107">(**DWORD**) Palabra de orden inferior especifica el nuevo ancho, en píxeles. Palabra de orden superior especifica el nuevo alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="37fad-107">(**DWORD**) Low-order WORD specifies the new width, in pixels; high-order WORD specifies the new height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="37fad-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="37fad-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="37fad-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="37fad-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="37fad-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="37fad-110">Default Action</span></span>

<span data-ttu-id="37fad-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37fad-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="37fad-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37fad-112">Remarks</span></span>

<span data-ttu-id="37fad-113">Los representadores de vídeo pueden enviar este evento si detectan un cambio en el tamaño de vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="37fad-113">Video renderers may send this event if they detect a change in the native video size.</span></span>

<span data-ttu-id="37fad-114">El [representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7) y el [representador de combinación de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9) envían este evento en modo de ventana, pero no en modo sin ventanas ni en modo sin procesar.</span><span class="sxs-lookup"><span data-stu-id="37fad-114">The [Video Mixing Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9) send this event in windowed mode, but not in windowless mode or renderless mode.</span></span> <span data-ttu-id="37fad-115">Para obtener más información sobre el modo de ventana en VMR, consulte [representación de vídeo](video-rendering.md).</span><span class="sxs-lookup"><span data-stu-id="37fad-115">For more information about windowed mode in the VMR, see [Video Rendering](video-rendering.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37fad-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37fad-116">Requirements</span></span>



| <span data-ttu-id="37fad-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="37fad-117">Requirement</span></span> | <span data-ttu-id="37fad-118">Value</span><span class="sxs-lookup"><span data-stu-id="37fad-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37fad-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37fad-119">Header</span></span><br/> | <dl> <span data-ttu-id="37fad-120"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="37fad-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37fad-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="37fad-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37fad-122">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="37fad-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="37fad-123">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="37fad-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




