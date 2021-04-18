---
title: Evento RenderingParametersUpdate
description: Se produce siempre que se actualiza cualquier conjunto de parámetros de control de representación en el DMR.
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- RenderingParametersUpdate Event media streaming API
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35e4898bae876babb0e5fbc1c4b9760eec6a9b62
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358878"
---
# <a name="renderingparametersupdate-event"></a><span data-ttu-id="8c767-104">Evento RenderingParametersUpdate</span><span class="sxs-lookup"><span data-stu-id="8c767-104">RenderingParametersUpdate event</span></span>

<span data-ttu-id="8c767-105">Se produce siempre que se actualiza cualquier conjunto de parámetros de control de representación en el DMR.</span><span class="sxs-lookup"><span data-stu-id="8c767-105">Occurs whenever any of a set of rendering control parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c767-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c767-106">Syntax</span></span>


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="8c767-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c767-107">Parameters</span></span>

<span data-ttu-id="8c767-108">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c767-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c767-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c767-109">Return value</span></span>

<span data-ttu-id="8c767-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="8c767-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c767-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c767-111">Remarks</span></span>

<span data-ttu-id="8c767-112">Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) mediante el método [**Add \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="8c767-112">To handle notifications from this event, register a [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) event handler function using the [**add\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) method.</span></span> <span data-ttu-id="8c767-113">Para anular el registro del controlador de eventos, use el método [**Remove \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="8c767-113">To unregister the event handler, use the [**remove\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) method.</span></span>

 

 