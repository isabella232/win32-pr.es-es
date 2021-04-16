---
description: Especifica la distancia de programación de un componente para el procesamiento de muestras.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689952"
---
# <a name="ec_sample_latency"></a><span data-ttu-id="9978f-103">\_latencia de ejemplo de EC \_</span><span class="sxs-lookup"><span data-stu-id="9978f-103">EC\_SAMPLE\_LATENCY</span></span>

<span data-ttu-id="9978f-104">Especifica la distancia de programación de un componente para el procesamiento de muestras.</span><span class="sxs-lookup"><span data-stu-id="9978f-104">Specifies how far behind schedule a component is for processing samples.</span></span>

## <a name="parameters"></a><span data-ttu-id="9978f-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9978f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9978f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9978f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9978f-107">(**\_ el tiempo de referencia const** \* ) hasta el punto en que se encuentra el componente, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="9978f-107">(**const REFERENCE\_TIME**\*) How far behind the component is, in 100-nanosecond units.</span></span> <span data-ttu-id="9978f-108">Si este valor es positivo, el componente está detrás de la programación.</span><span class="sxs-lookup"><span data-stu-id="9978f-108">If this value is positive, the component is behind schedule.</span></span> <span data-ttu-id="9978f-109">Si este valor es negativo, el componente está por encima de la programación.</span><span class="sxs-lookup"><span data-stu-id="9978f-109">If this value is negative, the component is ahead of schedule.</span></span>

</dd> <dt>

<span data-ttu-id="9978f-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9978f-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9978f-111">Cero.</span><span class="sxs-lookup"><span data-stu-id="9978f-111">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="9978f-112">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="9978f-112">Default Action</span></span>

<span data-ttu-id="9978f-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9978f-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="9978f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9978f-114">Remarks</span></span>

<span data-ttu-id="9978f-115">Un presentador personalizado para el filtro de [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR) puede enviar este mensaje a EVR para notificar a evr si el presentador está por detrás de la programación o por encima de la programación.</span><span class="sxs-lookup"><span data-stu-id="9978f-115">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR, to notify the EVR whether the presenter is behind schedule or ahead of schedule.</span></span>

<span data-ttu-id="9978f-116">La manera más sencilla de calcular *lParam1* es: *QPC Now*   *QPC Target*, donde *QPC Now* es ahora la hora de reloj y *QPC Target* es el tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="9978f-116">The simplest way to calculate *lParam1* is: *QPC now*   *QPC target*, where *QPC now* is the clock time now, and *QPC target* is the presentation time.</span></span>

## <a name="requirements"></a><span data-ttu-id="9978f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9978f-117">Requirements</span></span>



| <span data-ttu-id="9978f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9978f-118">Requirement</span></span> | <span data-ttu-id="9978f-119">Value</span><span class="sxs-lookup"><span data-stu-id="9978f-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9978f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9978f-120">Header</span></span><br/> | <dl> <span data-ttu-id="9978f-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="9978f-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9978f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9978f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9978f-123">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="9978f-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="9978f-124">Cómo escribir un presentador de EVR</span><span class="sxs-lookup"><span data-stu-id="9978f-124">How to Write an EVR Presenter</span></span>](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

