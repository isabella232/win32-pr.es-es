---
title: Interfaz INapEnforcementClientBinding (NapEnforcementClient. h)
description: Los clientes de cumplimiento utilizan para comunicarse con el NapAgent.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- Interfaz INapEnforcementClientBinding NAP
- Interfaz INapEnforcementClientBinding NAP, descripción
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905636"
---
# <a name="inapenforcementclientbinding-interface"></a>Interfaz INapEnforcementClientBinding

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapEnforcementClientBinding** proporciona métodos que los clientes de cumplimiento usan para comunicarse con NapAgent.

## <a name="members"></a>Miembros

La interfaz **INapEnforcementClientBinding** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapEnforcementClientBinding** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapEnforcementClientBinding** tiene estos métodos.



| Método                                                                                                                           | Descripción                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientBinding:: CreateConnection**](inapenforcementclientbinding-createconnection-method.md)                   | Lo usan los exigidos para crear objetos de conexión.<br/>                                                                                                                                                            |
| [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)                         | Lo usa el cliente de cumplimiento cuando necesita una solicitud de SoH para una conexión determinada.<br/>                                                                                                                   |
| [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md)                               | Inicia el servicio NapAgent. El cliente de cumplimiento debe llamar a este método antes de llamar a cualquier otro método de esta interfaz.<br/>                                                                            |
| [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | Se usa para informar a NapAgent de que una conexión a un cliente de cumplimiento ha dejado de funcionar.<br/>                                                                                                                      |
| [**INapEnforcementClientBinding::NotifySoHChangeFailure**](inapenforcementclientbinding-notifysohchangefailure-method.md)       | Lo usa el cliente de cumplimiento para informar a NapAgent de que no pudo procesar un [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)anterior.<br/> |
| [**INapEnforcementClientBinding::P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md)               | Lo usan los clientes de cumplimiento siempre que obtienen un BLOB de datos SoH-Response del servidor de cumplimiento.<br/>                                                                                                       |
| [**INapEnforcementClientBinding:: UnInitialize**](inapenforcementclientbinding-uninitialize-method.md)                           | Concluye el servicio NapAgent para esta conexión de cliente.<br/>                                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

Todas las API de esta interfaz devolverán RPC \_ E \_ desconectadas si NapAgent está detenido. Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.

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

 

