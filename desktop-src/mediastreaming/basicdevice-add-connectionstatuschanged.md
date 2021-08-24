---
title: BasicDevice.add_ConnectionStatusChanged método
description: Registra un controlador de eventos para el evento ConnectionStatusChanged. | BasicDevice.add_ConnectionStatusChanged método
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- add_ConnectionStatusChanged media streaming API
- add_ConnectionStatusChanged media streaming API, interfaz BasicDevice
- Interfaz basicDispositivo Media Streaming API , add_ConnectionStatusChanged método
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a416770a0ea3a4d317a2308fc9f5c9d940e89900aabbc7651ceb93b789454338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462265"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a>Método BasicDevice.add \_ ConnectionStatusChanged

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

Una [**función de controlador de eventos ConnectionStatusHandler.**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))

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

Para anular el registro del controlador de eventos registrado por este método, pase el *valor del token* al método Remove [**\_ ConnectionStatusChanged.**](basicdevice-remove-connectionstatuschanged.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

