---
title: Método DeviceController.CachedDevices
description: Recupera una colección de punteros de interfaz IBasicDevice que representa la vista en caché de todos los dispositivos DLNA detectables. | Método DeviceController.CachedDevices
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- Método CachedDevices de Media Streaming API
- Método CachedDevices de Media Streaming API, interfaz DeviceController
- Interfaz DeviceController Media Streaming API, método CachedDevices
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86e2c4209649450fb3a8df46cde151a0b9899cd26e58bfc0b35fd7ac6e7d02b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236365"
---
# <a name="devicecontrollercacheddevices-method"></a>Método DeviceController.CachedDevices

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

[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))
</dt> </dl>

 

