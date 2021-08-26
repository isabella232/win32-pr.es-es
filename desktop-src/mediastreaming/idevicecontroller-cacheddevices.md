---
title: Método IDeviceController CachedDevices
description: Recupera una colección de punteros de interfaz IBasicDevice que representa la vista en caché de todos los dispositivos DLNA detectables. | Método IDeviceController CachedDevices
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- Método CachedDevices de Media Streaming API
- Método CachedDevices de Media Streaming API, interfaz IDeviceController
- IDeviceController interface Media Streaming API , Método CachedDevices
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c624597fb88a45cc9ff91770f164e7c6e6e83ff5eb1b6369ded9d0fc1bbc225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952645"
---
# <a name="idevicecontrollercacheddevices-method"></a>IDeviceController::CachedDevices (método)

Recupera una colección de punteros de [**interfaz IBasicDevice**](ibasicdevice.md) que representa la vista en caché de todos los dispositivos DLNA detectables.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe una colección enumerable de punteros de interfaz [**IBasicDevice.**](ibasicdevice.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

