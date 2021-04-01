---
title: Método INapEnforcementClientCallback GetConnections (NapEnforcementClient. h)
description: Lo llama NapAgent y lo implementa el cliente de cumplimiento para devolver un conjunto de conexiones.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- Método GetConnections NAP
- Método GetConnections NAP, interfaz INapEnforcementClientCallback
- Interfaz INapEnforcementClientCallback NAP, método GetConnections
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
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905635"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a>INapEnforcementClientCallback:: GetConnections (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El NapAgent llama al método de devolución de llamada **INapEnforcementClientCallback:: GetConnections** y lo implementa el cliente de cumplimiento para devolver un conjunto de conexiones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*conexiones* \[ de enuncia\]
</dt> <dd>

Puntero al conjunto actual de [**conexiones**](connections-struct.md)mantenidas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método de devolución de llamada debe devolver uno de los siguientes códigos de error.



| Código devuelto                                                                                                | Descripción                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | Devuelve este valor si la operación se realizó correctamente.<br/>                                                                                                                                                              |
| <dl> <dt>**el \_ servidor RPC S \_ \_ no está disponible**</dt> </dl> | Al devolver este valor, el aplicador se quita de la lista Bound-SHA y la entrada de caché de NapAgent correspondiente que se va a vaciar. Después, el SHA con error puede volver a inicializarse con el NapAgent.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





