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
# <a name="devicedeparture-event"></a>Evento DeviceDeparture

Se produce cuando se quita un nuevo dispositivo de la lista de dispositivos devueltos por el método [**CachedDevices**](idevicecontroller-cacheddevices.md) .

## <a name="syntax"></a>Sintaxis


```C++
void DeviceDeparture();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) mediante el método [**Add \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) . Para anular el registro del controlador de eventos, use el método [**Remove \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) .

 

 