---
title: Interfaz INapEnforcementClientConnection (NapEnforcementClient. h)
description: Permite la administración de conexiones de cliente. | Interfaz INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- Interfaz INapEnforcementClientConnection NAP
- Interfaz INapEnforcementClientConnection NAP, descripción
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
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279990"
---
# <a name="inapenforcementclientconnection-interface"></a>Interfaz INapEnforcementClientConnection

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapEnforcementClientConnection** proporciona métodos que permiten la administración de conexiones de cliente.

> [!Note]  
> [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) hereda todos los métodos de esta interfaz y debe usarse en su lugar.

 

## <a name="members"></a>Miembros

La interfaz **INapEnforcementClientConnection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapEnforcementClientConnection** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapEnforcementClientConnection** tiene estos métodos.



| Método                                                                                                                           | Descripción                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection:: Getconnectionid (**](inapenforcementclientconnection-getconnectionid-method.md)               | Obtiene el identificador de conexión del cliente.<br/>                                                                                          |
| [**INapEnforcementClientConnection::GetCorrelationId**](inapenforcementclientconnection-getcorrelationid-method.md)             | Obtiene el identificador usado para correlacionar las solicitudes de SoH y las respuestas de SoH.<br/>                                                                  |
| [**INapEnforcementClientConnection::GetEnforcerPrivateData**](inapenforcementclientconnection-getenforcerprivatedata-method.md) | Lo utiliza el aplicador para obtener datos privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection:: GetFlags**](inapenforcementclientconnection-getflags-method.md)                             | Obtiene el valor de la marca que diferencia las respuestas por primera vez de las respuestas debido a SoHRequests almacenados en memoria caché por los imforcedores.<br/> |
| [**INapEnforcementClientConnection::GetIsolationInfo**](inapenforcementclientconnection-getisolationinfo-method.md)             | Se usa para obtener la información de aislamiento del cliente.<br/>                                                                              |
| [**INapEnforcementClientConnection::GetMaxSize**](inapenforcementclientconnection-getmaxsize-method.md)                         | Obtiene el tamaño máximo del paquete SoH para este cliente.<br/>                                                                       |
| [**INapEnforcementClientConnection::GetPrivateData**](inapenforcementclientconnection-getprivatedata-method.md)                 | Lo usa NapAgent para obtener datos privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection::GetSoHRequest**](inapenforcementclientconnection-getsohrequest-method.md)                   | Obtiene la solicitud de SoH.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::GetSoHResponse**](inapenforcementclientconnection-getsohresponse-method.md)                 | Obtiene el SoH-Response recibido por el cliente de cumplimiento.<br/>                                                                      |
| [**INapEnforcementClientConnection::GetStringCorrelationId**](inapenforcementclientconnection-getstringcorrelationid-method.md) | Obtiene la versión de cadena de CorrelationId. Se utiliza principalmente para fines de registro.<br/>                                             |
| [**INapEnforcementClientConnection:: Initialize**](inapenforcementclientconnection-initialize-method.md)                         | Inicializa la conexión.<br/>                                                                                                    |
| [**INapEnforcementClientConnection::SetConnectionId**](inapenforcementclientconnection-setconnectionid-method.md)               | Establece el identificador de conexión del cliente.<br/>                                                                                          |
| [**INapEnforcementClientConnection::SetCorrelationId**](inapenforcementclientconnection-setcorrelationid-method.md)             | Establece el identificador usado para correlacionar las solicitudes de SoH y las respuestas de SoH.<br/>                                                                  |
| [**INapEnforcementClientConnection::SetEnforcerPrivateData**](inapenforcementclientconnection-setenforcerprivatedata-method.md) | Lo utiliza el aplicador para establecer datos privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection:: SetFlags**](inapenforcementclientconnection-setflags-method.md)                             | Establece la marca que diferencia las respuestas por primera vez de las respuestas debido a SoHRequests almacenados en memoria caché por los incumplimientos.<br/>                  |
| [**INapEnforcementClientConnection::SetIsolationInfo**](inapenforcementclientconnection-setisolationinfo-method.md)             | Lo usa NapAgent para establecer la información de aislamiento del cliente.<br/>                                                           |
| [**INapEnforcementClientConnection::SetMaxSize**](inapenforcementclientconnection-setmaxsize-method.md)                         | Establece el tamaño máximo del paquete SoH para este cliente.<br/>                                                                       |
| [**INapEnforcementClientConnection::SetPrivateData**](inapenforcementclientconnection-setprivatedata-method.md)                 | Lo usa NapAgent para establecer datos privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetSoHRequest**](inapenforcementclientconnection-setsohrequest-method.md)                   | Establece la solicitud de SoH.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::SetSoHResponse**](inapenforcementclientconnection-setsohresponse-method.md)                 | Establece el SoH-Response y lo usa el cliente de cumplimiento al recibir un paquete.<br/>                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

