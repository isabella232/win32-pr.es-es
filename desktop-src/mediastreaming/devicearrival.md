---
title: Evento DeviceArrival
description: Se produce cuando se agrega un nuevo dispositivo a la lista de dispositivos devueltos por el método CachedDevices.
ms.assetid: C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2
keywords:
- DeviceArrival event Media Streaming API
topic_type:
- apiref
api_name:
- DeviceArrival
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed65c2b1c37eb91f9bf0a0c060fb76b85cd1f5b3d06b6ff1ab795ec89a0db6bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721215"
---
# <a name="devicearrival-event"></a>Evento DeviceArrival

Se produce cuando se agrega un nuevo dispositivo a la lista de dispositivos devueltos por el [**método CachedDevices.**](idevicecontroller-cacheddevices.md)

## <a name="syntax"></a>Sintaxis


```C++
void DeviceArrival();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**DeviceControllerControllerHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) mediante el [**método add \_ DeviceArrival.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) Para anular el registro del controlador de eventos, use [**el \_ método remove DeviceArrival.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival)

 

 