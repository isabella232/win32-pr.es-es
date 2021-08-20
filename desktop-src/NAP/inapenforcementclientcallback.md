---
title: Interfaz INapEnforcementClientCallback (NapEnforcementClient.h)
description: Los clientes de cumplimiento deben implementar para permitir que NapAgent se comunique con ellos.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- NAP de la interfaz INapEnforcementClientCallback
- Interfaz NAP de INapEnforcementClientCallback , descrita
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48c595918d28d912725353eb856de8f0af4541a68dabcb6f5a7cb0bb944496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134044"
---
# <a name="inapenforcementclientcallback-interface"></a>INapEnforcementClientCallback (interfaz)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **interfaz INapEnforcementClientCallback** proporciona métodos de devolución de llamada que los clientes de cumplimiento deben implementar para permitir que NapAgent se comunique con ellos.

## <a name="members"></a>Miembros

La **interfaz INapEnforcementClientCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapEnforcementClientCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapEnforcementClientCallback** tiene estos métodos.



| Método                                                                                                         | Descripción                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientCallback::GetConnections**](inapenforcementclientcallback-getconnections-method.md)   | Lo usa NapAgent para recuperar las conexiones.<br/>                         |
| [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) | Lo usa NapAgent para informar al cliente de cumplimiento de los cambios de SoH.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



 

