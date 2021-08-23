---
title: Interfaz INapEnforcementClientConnection (NapEnforcementClient.h)
description: Permitir la administración de conexiones de cliente. | Interfaz INapEnforcementClientConnection (NapEnforcementClient.h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- NAP de la interfaz INapEnforcementClientConnection
- Interfaz NAP de INapEnforcementClientConnection , descrita
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba017ca0948c5769466be9ad43ef68dc5ff60e75ecea430c96a1e8b0c36ab1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686255"
---
# <a name="inapenforcementclientconnection-interface"></a>Interfaz INapEnforcementClientConnection

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapEnforcementClientConnection proporciona** métodos que permiten la administración de conexiones de cliente.

> [!Note]  
> [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) hereda todos los métodos de esta interfaz y se debe usar en su lugar.

 

## <a name="members"></a>Miembros

La **interfaz INapEnforcementClientConnection** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapEnforcementClientConnection** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapEnforcementClientConnection** tiene estos métodos.



| Método                                                                                                                           | Descripción                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection::GetConnectionId**](inapenforcementclientconnection-getconnectionid-method.md)               | Obtiene el identificador de conexión del cliente.<br/>                                                                                          |
| [**INapEnforcementClientConnection::GetCorrelationId**](inapenforcementclientconnection-getcorrelationid-method.md)             | Obtiene el identificador utilizado para poner en correlación soH-requests y SoH-responses.<br/>                                                                  |
| [**INapEnforcementClientConnection::GetEnforcerPrivateData**](inapenforcementclientconnection-getenforcerprivatedata-method.md) | Usado por el ejecutor para obtener datos privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection::GetFlags**](inapenforcementclientconnection-getflags-method.md)                             | Obtiene el valor de la marca que diferencia las respuestas por primera vez de las respuestas debido a las solicitudes SoHRequest almacenadas en caché por los aplicadores.<br/> |
| [**INapEnforcementClientConnection::GetIsolationInfo**](inapenforcementclientconnection-getisolationinfo-method.md)             | Los usados obtienen la información de aislamiento del cliente.<br/>                                                                              |
| [**INapEnforcementClientConnection::GetMaxSize**](inapenforcementclientconnection-getmaxsize-method.md)                         | Obtiene el tamaño máximo del paquete SoH para este cliente.<br/>                                                                       |
| [**INapEnforcementClientConnection::GetPrivateData**](inapenforcementclientconnection-getprivatedata-method.md)                 | Lo usa NapAgent para obtener datos privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection::GetSoHRequest**](inapenforcementclientconnection-getsohrequest-method.md)                   | Obtiene la solicitud SoH.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::GetSoHResponse**](inapenforcementclientconnection-getsohresponse-method.md)                 | Obtiene el SoH-Response recibido por el cliente de cumplimiento.<br/>                                                                      |
| [**INapEnforcementClientConnection::GetStringCorrelationId**](inapenforcementclientconnection-getstringcorrelationid-method.md) | Obtiene la versión de cadena de CorrelationId. Se usa principalmente con fines de registro.<br/>                                             |
| [**INapEnforcementClientConnection::Initialize**](inapenforcementclientconnection-initialize-method.md)                         | Inicializa la conexión.<br/>                                                                                                    |
| [**INapEnforcementClientConnection::SetConnectionId**](inapenforcementclientconnection-setconnectionid-method.md)               | Establece el identificador de conexión del cliente.<br/>                                                                                          |
| [**INapEnforcementClientConnection::SetCorrelationId**](inapenforcementclientconnection-setcorrelationid-method.md)             | Establece el identificador que se usa para correlacionar soh-requests y soH-responses.<br/>                                                                  |
| [**INapEnforcementClientConnection::SetEnforcerPrivateData**](inapenforcementclientconnection-setenforcerprivatedata-method.md) | Usado por el ejecutor para establecer datos privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetFlags**](inapenforcementclientconnection-setflags-method.md)                             | Establece la marca que diferencia las respuestas por primera vez de las respuestas debido a soHRequests almacenados en caché por los aplicadores.<br/>                  |
| [**INapEnforcementClientConnection::SetIsolationInfo**](inapenforcementclientconnection-setisolationinfo-method.md)             | Lo usa NapAgent para establecer la información de aislamiento del cliente.<br/>                                                           |
| [**INapEnforcementClientConnection::SetMaxSize**](inapenforcementclientconnection-setmaxsize-method.md)                         | Establece el tamaño máximo del paquete SoH para este cliente.<br/>                                                                       |
| [**INapEnforcementClientConnection::SetPrivateData**](inapenforcementclientconnection-setprivatedata-method.md)                 | Lo usa NapAgent para establecer datos privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetSoHRequest**](inapenforcementclientconnection-setsohrequest-method.md)                   | Establece la solicitud SoH.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::SetSoHResponse**](inapenforcementclientconnection-setsohresponse-method.md)                 | Establece el SoH-Response y lo usa el cliente de cumplimiento al recibir un paquete.<br/>                                             |



 

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

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

