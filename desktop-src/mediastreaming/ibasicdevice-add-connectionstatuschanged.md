---
title: Método add_ConnectionStatusChanged IBasicDevice
description: Registra un controlador de eventos para el evento ConnectionStatusChanged. | Método add_ConnectionStatusChanged IBasicDevice
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- método add_ConnectionStatusChanged API de streaming multimedia
- método add_ConnectionStatusChanged API de streaming multimedia, interfaz IBasicDevice
- IBasicDevice interface media streaming API, método add_ConnectionStatusChanged
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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698150"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a>IBasicDevice:: Add \_ ConnectionStatusChanged (método)

Registra un controlador de eventos para el evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*controlador* \[ de de\]
</dt> <dd>

Función de controlador de eventos [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .

</dd> <dt>

*token* \[ de out, retval\]
</dt> <dd>

Referencia a un token que se puede usar para anular el registro del controlador de eventos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Para anular el registro del controlador de eventos registrado por este método, pase el valor del *token* al método [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

