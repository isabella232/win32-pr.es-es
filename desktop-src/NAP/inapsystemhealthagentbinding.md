---
title: Interfaz INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Los Sha usan para comunicarse con el NapAgent. | Interfaz INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- Interfaz INapSystemHealthAgentBinding NAP
- Interfaz INapSystemHealthAgentBinding NAP, descripción
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38d1331996e34c6879fc2e98ce566ce6802527a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678759"
---
# <a name="inapsystemhealthagentbinding-interface"></a>Interfaz INapSystemHealthAgentBinding

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapSystemHealthAgentBinding** proporciona métodos que los Sha usan para comunicarse con NapAgent.

> [!Note]  
> [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) hereda todos los métodos de esta interfaz y debe usarse en su lugar.

 

## <a name="members"></a>Miembros

La interfaz **INapSystemHealthAgentBinding** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthAgentBinding** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapSystemHealthAgentBinding** tiene estos métodos.



| Método                                                                                                                     | Descripción                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding::FlushCache**](inapsystemhealthagentbinding-flushcache-method.md)                         | Lo llama un SHA para vaciar la memoria caché de SoH.<br/>                                                |
| [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | Lo llaman los Sha para determinar el estado de aislamiento del sistema.<br/>                                 |
| [**INapSystemHealthAgentBinding:: Initialize**](inapsystemhealthagentbinding-initialize-method.md)                         | Inicializa SHA y enlaza el SHA al servicio NapAgent. <br/>                         |
| [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md)               | Lo llaman los Sha cuando cambia el SoH.<br/>                                                  |
| [**INapSystemHealthAgentBinding:: UnInitialize**](inapsystemhealthagentbinding-uninitialize-method.md)                     | Lo llaman los Sha para hacer que el NapAgent libere todas sus referencias a punteros COM SHA.<br/> |



 

## <a name="remarks"></a>Observaciones

Todas las API de esta interfaz devolverán **RPC \_ E \_ desconectadas** si NapAgent está detenido. Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

