---
title: Método INapEnforcementClientConnection GetConnectionId (NapEnforcementClient.h)
description: Se usa para obtener el identificador de conexión único del cliente.
ms.assetid: bf744aa6-5786-473f-9508-db4ee0c75578
keywords:
- Método NAP de GetConnectionId
- Método NAP de GetConnectionId, interfaz INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , GetConnectionId method
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee645e49a8e8f9389fa5c43bd1f4453d19854fc43a8a31a2e720cc09a38e99ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134024"
---
# <a name="inapenforcementclientconnectiongetconnectionid-method"></a>INapEnforcementClientConnection::GetConnectionId (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapEnforcementClientConnection::GetConnectionId** se usa para obtener el identificador de conexión único del cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConnectionId(
  [out] ConnectionId **connectionId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*connectionId* \[ out\]
</dt> <dd>

Puntero a un puntero a un [**ConnectionId**](nap-datatypes.md) que identifica de forma única esta conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

El identificador de conexión se usa principalmente con fines de registro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





