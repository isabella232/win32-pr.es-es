---
title: Interfaz INapClientManagement (NapManagement. h)
description: Proporciona métodos para la administración del cliente de NAP. | Interfaz INapClientManagement (NapManagement. h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- Interfaz INapClientManagement NAP
- Interfaz INapClientManagement NAP, descripción
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe90158d6f1e9a864f7d19448a412d70890133d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003660"
---
# <a name="inapclientmanagement-interface"></a>Interfaz INapClientManagement

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La interfaz **INapClientManagement** proporciona métodos para la administración del cliente de NAP.

> [!Note]  
> [**INapClientManagement2**](inapclientmanagement2.md) hereda todos los métodos de esta interfaz y debe usarse en su lugar.

 

## <a name="members"></a>Miembros

La interfaz **INapClientManagement** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapClientManagement** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapClientManagement** tiene estos métodos.



| Método                                                                                                                | Descripción                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**INapClientManagement::GetNapClientInfo**](inapclientmanagement-getnapclientinfo.md)                               | Recupera información sobre un cliente de NAP.<br/>                          |
| [**INapClientManagement::GetRegisteredEnforcementClients**](inapclientmanagement-getregisteredenforcementclients.md) | Recupera información acerca de los clientes de cumplimiento registrados.<br/>    |
| [**INapClientManagement::GetRegisteredSystemHealthAgents**](inapclientmanagement-getregisteredsystemhealthagents.md) | Recupera información sobre un SHA registrado.<br/>                       |
| [**INapClientManagement::GetSystemIsolationInfo**](inapclientmanagement-getsystemisolationinfo.md)                   | Recupera información sobre el estado de aislamiento del cliente NAP.<br/> |
| [**INapClientManagement::RegisterEnforcementClient**](inapclientmanagement-registerenforcementclient.md)             | Registra un cliente de cumplimiento con el sistema NAP.<br/>               |
| [**INapClientManagement::RegisterSystemHealthAgent**](inapclientmanagement-registersystemhealthagent.md)             | Registra un SHA con el sistema NAP.<br/>                              |
| [**INapClientManagement::UnregisterEnforcementClient**](inapclientmanagement-unregisterenforcementclient.md)         | Anula el registro de un cliente de cumplimiento con el sistema NAP.<br/>             |
| [**INapClientManagement::UnregisterSystemHealthAgent**](inapclientmanagement-unregistersystemhealthagent.md)         | Anula el registro de un SHA con el sistema NAP.<br/>                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

