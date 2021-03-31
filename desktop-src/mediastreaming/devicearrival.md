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
# <a name="devicearrival-event"></a>Evento DeviceArrival

Se produce cuando se agrega un nuevo dispositivo a la lista de dispositivos devueltos por el método [**CachedDevices**](idevicecontroller-cacheddevices.md) .

## <a name="syntax"></a>Sintaxis


```C++
void DeviceArrival();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) mediante el método [**Add \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) . Para anular el registro del controlador de eventos, use el método [**Remove \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) .

 

 