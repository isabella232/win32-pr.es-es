---
title: Interfaz INapClientManagement (NapManagement.h)
description: Proporciona métodos para la administración de clientes NAP. | Interfaz INapClientManagement (NapManagement.h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- NAP de la interfaz INapClientManagement
- Interfaz NAP de INapClientManagement , descrita
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
ms.openlocfilehash: 56a9d338cdaad8ed46fd3c3c730ca3ae4c2065cda9803c283ae262addd939713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622122"
---
# <a name="inapclientmanagement-interface"></a>Interfaz INapClientManagement

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **interfaz INapClientManagement proporciona métodos** para la administración de clientes NAP.

> [!Note]  
> [**INapClientManagement2**](inapclientmanagement2.md) hereda todos los métodos de esta interfaz y se debe usar en su lugar.

 

## <a name="members"></a>Miembros

La **interfaz INapClientManagement** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapClientManagement** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapClientManagement** tiene estos métodos.



| Método                                                                                                                | Descripción                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**INapClientManagement::GetNapClientInfo**](inapclientmanagement-getnapclientinfo.md)                               | Recupera información sobre un cliente NAP.<br/>                          |
| [**INapClientManagement::GetRegisteredEnforcementClients**](inapclientmanagement-getregisteredenforcementclients.md) | Recupera información sobre los clientes de cumplimiento registrados.<br/>    |
| [**INapClientManagement::GetRegisteredSystemHealthAgents**](inapclientmanagement-getregisteredsystemhealthagents.md) | Recupera información sobre un SHA registrado.<br/>                       |
| [**INapClientManagement::GetSystemIsolationInfo**](inapclientmanagement-getsystemisolationinfo.md)                   | Recupera información sobre el estado de aislamiento del cliente nap.<br/> |
| [**INapClientManagement::RegisterEnforcementClient**](inapclientmanagement-registerenforcementclient.md)             | Registra un cliente de cumplimiento con el sistema NAP.<br/>               |
| [**INapClientManagement::RegisterSystemHealthAgent**](inapclientmanagement-registersystemhealthagent.md)             | Registra un SHA con el sistema NAP.<br/>                              |
| [**INapClientManagement::UnregisterEnforcementClient**](inapclientmanagement-unregisterenforcementclient.md)         | Anula el registro de un cliente de cumplimiento con el sistema NAP.<br/>             |
| [**INapClientManagement::UnregisterSystemHealthAgent**](inapclientmanagement-unregistersystemhealthagent.md)         | Anula el registro de un SHA con el sistema NAP.<br/>                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

