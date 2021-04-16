---
description: Indica la cantidad de tiempo que un componente está tomando para procesar cada ejemplo.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d97514b4d2851f619f89f42e644766d50b7d25f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678913"
---
# <a name="ec_processing_latency"></a><span data-ttu-id="ddba3-103">\_latencia de procesamiento de EC \_</span><span class="sxs-lookup"><span data-stu-id="ddba3-103">EC\_PROCESSING\_LATENCY</span></span>

<span data-ttu-id="ddba3-104">Indica la cantidad de tiempo que un componente está tomando para procesar cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ddba3-104">Indicates the amount of time that a component is taking to process each sample.</span></span>

## <a name="parameters"></a><span data-ttu-id="ddba3-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddba3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddba3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ddba3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ddba3-107">(**\_ tiempo de referencia const** \* ) la cantidad de tiempo que se va a procesar cada muestra, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="ddba3-107">(**const REFERENCE\_TIME**\*) The amount of time to process each sample, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="ddba3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ddba3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ddba3-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="ddba3-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ddba3-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="ddba3-110">Default Action</span></span>

<span data-ttu-id="ddba3-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ddba3-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddba3-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddba3-112">Remarks</span></span>

<span data-ttu-id="ddba3-113">Un presentador del filtro de [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR) puede enviar este mensaje a EVR para notificar a EVR sobre la latencia de procesamiento del presentador.</span><span class="sxs-lookup"><span data-stu-id="ddba3-113">A presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR to notify the EVR about the presenter's processing latency.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddba3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddba3-114">Requirements</span></span>



| <span data-ttu-id="ddba3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddba3-115">Requirement</span></span> | <span data-ttu-id="ddba3-116">Value</span><span class="sxs-lookup"><span data-stu-id="ddba3-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ddba3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddba3-117">Header</span></span><br/> | <dl> <span data-ttu-id="ddba3-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddba3-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddba3-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddba3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddba3-120">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="ddba3-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ddba3-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="ddba3-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




