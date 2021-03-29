---
title: IDeviceController CachedDevices, método
description: Recupera una colección de punteros de interfaz IBasicDevice que representa la vista almacenada en memoria caché de todos los dispositivos DLNA detectables. | IDeviceController CachedDevices, método
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- Método CachedDevices API de streaming de multimedia
- Método CachedDevices API de streaming de multimedia, interfaz IDeviceController
- Interfaz IDeviceController API de streaming de multimedia, método CachedDevices
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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003734"
---
# <a name="idevicecontrollercacheddevices-method"></a>IDeviceController:: CachedDevices (método)

Recupera una colección de punteros de interfaz [**IBasicDevice**](ibasicdevice.md) que representa la vista almacenada en memoria caché de todos los dispositivos DLNA detectables.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Recibe una colección enumerable de punteros de interfaz [**IBasicDevice**](ibasicdevice.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

