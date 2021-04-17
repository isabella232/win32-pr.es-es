---
title: Evento DeviceDeparture
description: Se produce cuando se quita un nuevo dispositivo de la lista de dispositivos devueltos por el método CachedDevices.
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- DeviceDeparture Event media streaming API
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e225afcbe8b373b22584eaa3d9fcb09e1eff29c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714367"
---
# <a name="devicedeparture-event"></a><span data-ttu-id="7b128-104">Evento DeviceDeparture</span><span class="sxs-lookup"><span data-stu-id="7b128-104">DeviceDeparture event</span></span>

<span data-ttu-id="7b128-105">Se produce cuando se quita un nuevo dispositivo de la lista de dispositivos devueltos por el método [**CachedDevices**](idevicecontroller-cacheddevices.md) .</span><span class="sxs-lookup"><span data-stu-id="7b128-105">Occurs when a new device is removed from the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b128-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b128-106">Syntax</span></span>


```C++
void DeviceDeparture();
```



## <a name="parameters"></a><span data-ttu-id="7b128-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b128-107">Parameters</span></span>

<span data-ttu-id="7b128-108">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7b128-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b128-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b128-109">Return value</span></span>

<span data-ttu-id="7b128-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="7b128-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b128-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b128-111">Remarks</span></span>

<span data-ttu-id="7b128-112">Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) mediante el método [**Add \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) .</span><span class="sxs-lookup"><span data-stu-id="7b128-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) method.</span></span> <span data-ttu-id="7b128-113">Para anular el registro del controlador de eventos, use el método [**Remove \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) .</span><span class="sxs-lookup"><span data-stu-id="7b128-113">To unregister the event handler, use the [**remove\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) method.</span></span>

 

 