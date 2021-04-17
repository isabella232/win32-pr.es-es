---
title: DeviceController. CachedDevices, método
description: Recupera una colección de punteros de interfaz IBasicDevice que representa la vista almacenada en memoria caché de todos los dispositivos DLNA detectables. | DeviceController. CachedDevices, método
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- Método CachedDevices API de streaming de multimedia
- Método CachedDevices API de streaming de multimedia, interfaz DeviceController
- Interfaz DeviceController API de streaming de multimedia, método CachedDevices
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0bb39e03a9788e0c444f682b61d39fc1c65781b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717475"
---
# <a name="devicecontrollercacheddevices-method"></a>DeviceController. CachedDevices, método

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

[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))
</dt> </dl>

 

