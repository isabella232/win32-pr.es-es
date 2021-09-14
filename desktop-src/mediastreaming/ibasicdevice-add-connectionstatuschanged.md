---
title: IBasicDevice add_ConnectionStatusChanged método
description: Registra un controlador de eventos para el evento ConnectionStatusChanged. | IBasicDevice add_ConnectionStatusChanged método
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- add_ConnectionStatusChanged media streaming API
- add_ConnectionStatusChanged media streaming API, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , add_ConnectionStatusChanged método
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0028e6f3dad1670974178b0f07a59f74dffdc06f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248511"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a>IBasicDevice::add \_ ConnectionStatusChanged (método)

Registra un controlador de eventos para el [**evento ConnectionStatusChanged.**](connectionstatuschanged.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*controlador* \[ En\]
</dt> <dd>

Una función de controlador de eventos [**ConnectionStatusHandler.**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))

</dd> <dt>

*token* \[ out, retval\]
</dt> <dd>

Referencia a un token que se puede usar para anular el registro del controlador de eventos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Para anular el registro del controlador de eventos registrado por este método, pase el *valor del token* al método Remove [**\_ ConnectionStatusChanged.**](ibasicdevice-remove-connectionstatuschanged.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

