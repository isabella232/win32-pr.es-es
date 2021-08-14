---
title: Método INapEnforcementClientCallback GetConnections (NapEnforcementClient.h)
description: NapAgent llama a y lo implementa el cliente de cumplimiento para devolver un conjunto de conexiones.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- Método NAP de GetConnections
- Método Nap de GetConnections, interfaz INapEnforcementClientCallback
- INapEnforcementClientCallback interface NAP , Método GetConnections
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f6c6fdb4adc416cb25fa0e402c8fee2d8baf3270400f15a8de67966eff7a9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134034"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a>INapEnforcementClientCallback::GetConnections (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

NapAgent llama al método de devolución de llamada **INapEnforcementClientCallback::GetConnections** y lo implementa el cliente de cumplimiento para devolver un conjunto de conexiones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*conexiones* \[ out\]
</dt> <dd>

Puntero al conjunto actual de conexiones [**mantenidas.**](connections-struct.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método de devolución de llamada debe devolver uno de los siguientes códigos de error.



| Código devuelto                                                                                                | Descripción                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Devuelve este valor si la operación se ha correcto.<br/>                                                                                                                                                              |
| <dl> <dt>**SERVIDOR \_ RPC S NO \_ \_ DISPONIBLE**</dt> </dl> | La devolución de este valor hace que el ejecutor se quite de la lista bound-SHA y se vacíe la entrada de caché de NapAgent correspondiente. Después, el SHA con errores puede volver a inicializarse con NapAgent.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





