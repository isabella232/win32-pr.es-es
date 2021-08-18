---
title: Evento DeviceDeparture
description: Se produce cuando se quita un nuevo dispositivo de la lista de dispositivos devueltos por el método CachedDevices.
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- DeviceDeparture event Media Streaming API
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496fa0fcae3cba51228b37b5f06eb9b06c416322aad22f77be542274088eae32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712955"
---
# <a name="devicedeparture-event"></a>Evento DeviceDeparture

Se produce cuando se quita un nuevo dispositivo de la lista de dispositivos devueltos por el [**método CachedDevices.**](idevicecontroller-cacheddevices.md)

## <a name="syntax"></a>Sintaxis


```C++
void DeviceDeparture();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**DeviceControllerHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) mediante el [**método add \_ DeviceDeparture.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) Para anular el registro del controlador de eventos, use [**el \_ método remove DeviceDeparture.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture)

 

 