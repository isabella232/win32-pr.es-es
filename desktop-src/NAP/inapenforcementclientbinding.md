---
title: Interfaz INapEnforcementClientBinding (NapEnforcementClient.h)
description: Los clientes de cumplimiento usan para comunicarse con NapAgent.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- NAP de la interfaz INapEnforcementClientBinding
- Interfaz NAP de INapEnforcementClientBinding , descrita
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362172"
---
# <a name="inapenforcementclientbinding-interface"></a>INapEnforcementClientBinding (interfaz)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapEnforcementClientBinding proporciona** métodos que los clientes de cumplimiento usan para comunicarse con NapAgent.

## <a name="members"></a>Members

La **interfaz INapEnforcementClientBinding** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapEnforcementClientBinding** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapEnforcementClientBinding** tiene estos métodos.



| Método                                                                                                                           | Descripción                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientBinding::CreateConnection**](inapenforcementclientbinding-createconnection-method.md)                   | Usado por los aplicadores para crear objetos de conexión.<br/>                                                                                                                                                            |
| [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)                         | Lo usa el cliente de cumplimiento cuando necesita una solicitud soH para una conexión determinada.<br/>                                                                                                                   |
| [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md)                               | Inicia el servicio NapAgent. El cliente de cumplimiento debe llamar a este método antes de llamar a cualquier otro método de esta interfaz.<br/>                                                                            |
| [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | Se usa para informar a NapAgent de que una conexión a un cliente de cumplimiento ha desaparecido.<br/>                                                                                                                      |
| [**INapEnforcementClientBinding::NotifySoHChangeFailure**](inapenforcementclientbinding-notifysohchangefailure-method.md)       | Usado por el cliente de cumplimiento para informar a NapAgent de que no pudo procesar un [**INapEnforcementClientCallback::NotifySoHChange anterior.**](inapenforcementclientcallback-notifysohchange-method.md)<br/> |
| [**INapEnforcementClientBinding::P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md)               | Los clientes de cumplimiento usan cada vez que obtienen un blob SoH-Response datos del servidor de cumplimiento.<br/>                                                                                                       |
| [**INapEnforcementClientBinding::Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)                           | Concluye el servicio NapAgent para esta conexión de cliente.<br/>                                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

Todas las API de esta interfaz devolverán RPC \_ E \_ DISCONNECTED si napAgent está detenido. Este objeto se recuperará automáticamente y se volverá a conectar a NapAgent, una vez que se reinicie.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

