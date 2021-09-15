---
title: Método IDeviceController CachedDevices
description: Recupera una colección de punteros de interfaz IBasicDevice que representa la vista en caché de todos los dispositivos DLNA reconocibles. | Método IDeviceController CachedDevices
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- Método CachedDevices de Media Streaming API
- Método CachedDevices de Media Streaming API, interfaz IDeviceController
- IDeviceController interface Media Streaming API , CachedDevices method
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468576"
---
# <a name="idevicecontrollercacheddevices-method"></a>IDeviceController::CachedDevices (método)

Recupera una colección de punteros de [**interfaz IBasicDevice**](ibasicdevice.md) que representa la vista en caché de todos los dispositivos DLNA reconocibles.

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

 

