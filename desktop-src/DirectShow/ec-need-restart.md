---
description: Un filtro solicita que el gráfico se reinicie.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678918"
---
# <a name="ec_need_restart"></a><span data-ttu-id="945af-103">EC \_ necesidad de \_ reiniciar</span><span class="sxs-lookup"><span data-stu-id="945af-103">EC\_NEED\_RESTART</span></span>

<span data-ttu-id="945af-104">Un filtro solicita que el gráfico se reinicie.</span><span class="sxs-lookup"><span data-stu-id="945af-104">A filter is requesting that the graph be restarted.</span></span>

## <a name="parameters"></a><span data-ttu-id="945af-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="945af-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="945af-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="945af-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="945af-107">Cero.</span><span class="sxs-lookup"><span data-stu-id="945af-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="945af-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="945af-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="945af-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="945af-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="945af-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="945af-110">Default Action</span></span>

<span data-ttu-id="945af-111">El administrador de gráficos de filtro detiene y reinicia el gráfico.</span><span class="sxs-lookup"><span data-stu-id="945af-111">The filter graph manager pauses and restarts the graph.</span></span> <span data-ttu-id="945af-112">No pasa el evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="945af-112">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="945af-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="945af-113">Remarks</span></span>

<span data-ttu-id="945af-114">Si un filtro rechaza un ejemplo en medio de una secuencia, el PIN ascendente dejará de entregar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="945af-114">If a filter rejects a sample in the middle of a stream, the upstream pin will stop delivering samples.</span></span> <span data-ttu-id="945af-115">El filtro puede reiniciar el flujo mediante el envío de este evento.</span><span class="sxs-lookup"><span data-stu-id="945af-115">The filter can restart the stream by sending this event.</span></span> <span data-ttu-id="945af-116">Por ejemplo, el representador de audio podría perder el acceso al dispositivo de sonido, porque una ventana de vídeo ha perdido el foco.</span><span class="sxs-lookup"><span data-stu-id="945af-116">For example, the audio renderer might lose access to the sound device, because a video window has lost focus.</span></span> <span data-ttu-id="945af-117">En ese momento, el representador de audio comienza a rechazar los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="945af-117">At that point, the audio renderer starts rejecting samples.</span></span> <span data-ttu-id="945af-118">Cuando recupera el acceso al dispositivo de sonido, envía este evento para reiniciar la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="945af-118">When it regains access to the sound device, it sends this event to restart the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="945af-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="945af-119">Requirements</span></span>



| <span data-ttu-id="945af-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="945af-120">Requirement</span></span> | <span data-ttu-id="945af-121">Value</span><span class="sxs-lookup"><span data-stu-id="945af-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="945af-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="945af-122">Header</span></span><br/> | <dl> <span data-ttu-id="945af-123"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="945af-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="945af-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="945af-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="945af-125">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="945af-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="945af-126">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="945af-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




