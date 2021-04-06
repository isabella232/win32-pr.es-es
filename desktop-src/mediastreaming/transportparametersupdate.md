---
title: Evento TransportParametersUpdate
description: Se produce siempre que se actualiza cualquier conjunto de parámetros de transporte en el DMR.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- TransportParametersUpdate Event media streaming API
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58df04862275af5da8714f8a954dc5b127f833f2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904582"
---
# <a name="transportparametersupdate-event"></a><span data-ttu-id="45f55-104">Evento TransportParametersUpdate</span><span class="sxs-lookup"><span data-stu-id="45f55-104">TransportParametersUpdate event</span></span>

<span data-ttu-id="45f55-105">Se produce siempre que se actualiza cualquier conjunto de parámetros de transporte en el DMR.</span><span class="sxs-lookup"><span data-stu-id="45f55-105">Occurs whenever any of a set of transport parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f55-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45f55-106">Syntax</span></span>


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="45f55-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45f55-107">Parameters</span></span>

<span data-ttu-id="45f55-108">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="45f55-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="45f55-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45f55-109">Return value</span></span>

<span data-ttu-id="45f55-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="45f55-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45f55-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45f55-111">Remarks</span></span>

<span data-ttu-id="45f55-112">Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) mediante el método [**Add \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="45f55-112">To handle notifications from this event, register a [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) event handler function using the [**add\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) method.</span></span> <span data-ttu-id="45f55-113">Para anular el registro del controlador de eventos, use el método [**Remove \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="45f55-113">To unregister the event handler, use the [**remove\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) method.</span></span>

 

 