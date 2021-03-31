---
title: Evento DeviceArrival
description: Se produce cuando se agrega un nuevo dispositivo a la lista de dispositivos devueltos por el método CachedDevices.
ms.assetid: C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2
keywords:
- DeviceArrival Event media streaming API
topic_type:
- apiref
api_name:
- DeviceArrival
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79fbdd68ae6c77c6a0f3e7bbd3cf976b5d056987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790197"
---
# <a name="devicearrival-event"></a><span data-ttu-id="06fe8-104">Evento DeviceArrival</span><span class="sxs-lookup"><span data-stu-id="06fe8-104">DeviceArrival event</span></span>

<span data-ttu-id="06fe8-105">Se produce cuando se agrega un nuevo dispositivo a la lista de dispositivos devueltos por el método [**CachedDevices**](idevicecontroller-cacheddevices.md) .</span><span class="sxs-lookup"><span data-stu-id="06fe8-105">Occurs when a new device is added to the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06fe8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06fe8-106">Syntax</span></span>


```C++
void DeviceArrival();
```



## <a name="parameters"></a><span data-ttu-id="06fe8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06fe8-107">Parameters</span></span>

<span data-ttu-id="06fe8-108">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="06fe8-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06fe8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06fe8-109">Return value</span></span>

<span data-ttu-id="06fe8-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="06fe8-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06fe8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06fe8-111">Remarks</span></span>

<span data-ttu-id="06fe8-112">Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) mediante el método [**Add \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) .</span><span class="sxs-lookup"><span data-stu-id="06fe8-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) method.</span></span> <span data-ttu-id="06fe8-113">Para anular el registro del controlador de eventos, use el método [**Remove \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) .</span><span class="sxs-lookup"><span data-stu-id="06fe8-113">To unregister the event handler, use the [**remove\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) method.</span></span>

 

 