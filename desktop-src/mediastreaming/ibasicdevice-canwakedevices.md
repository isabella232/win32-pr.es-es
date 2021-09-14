---
title: Método IBasicDevice CanWakeDevices
description: Recupera un valor que indica si el dispositivo puede reactivar.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- Método CanWakeDevices de Media Streaming API
- Api de streaming multimedia del método CanWakeDevices, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , método CanWakeDevices
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248504"
---
# <a name="ibasicdevicecanwakedevices-method"></a>IBasicDevice::CanWakeDevices (método)

Recupera un valor que indica si el dispositivo puede reactivar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe un puntero a un valor booleano que es **True** si el dispositivo puede reactivar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





