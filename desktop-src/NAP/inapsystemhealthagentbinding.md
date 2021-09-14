---
title: Interfaz INapSystemHealthAgentBinding (NapSystemHealthAgent.h)
description: Los SHA usan para comunicarse con NapAgent. | Interfaz INapSystemHealthAgentBinding (NapSystemHealthAgent.h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- NAP de la interfaz INapSystemHealthAgentBinding
- Interfaz NAP de INapSystemHealthAgentBinding , descrita
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071652"
---
# <a name="inapsystemhealthagentbinding-interface"></a>INapSystemHealthAgentBinding (interfaz)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapSystemHealthAgentBinding proporciona métodos** que los SHA usan para comunicarse con NapAgent.

> [!Note]  
> [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) hereda todos los métodos de esta interfaz y se debe usar en su lugar.

 

## <a name="members"></a>Members

La **interfaz INapSystemHealthAgentBinding** hereda de [**la interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthAgentBinding** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapSystemHealthAgentBinding** tiene estos métodos.



| Método                                                                                                                     | Descripción                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding::FlushCache**](inapsystemhealthagentbinding-flushcache-method.md)                         | Lo llama un SHA para vaciar su caché de SoH.<br/>                                                |
| [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | Lo llaman las SHA para determinar el estado de aislamiento del sistema.<br/>                                 |
| [**INapSystemHealthAgentBinding::Initialize**](inapsystemhealthagentbinding-initialize-method.md)                         | Inicializa sha y enlaza sha al servicio NapAgent. <br/>                         |
| [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md)               | Lo llaman las SHA cuando su SoH cambia.<br/>                                                  |
| [**INapSystemHealthAgentBinding::Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md)                     | Lo llaman los SHA para hacer que NapAgent libere todas sus referencias a punteros SHA COM.<br/> |



 

## <a name="remarks"></a>Observaciones

Todas las API de esta interfaz **devolverán RPC \_ E \_ DISCONNECTED** si napAgent está detenido. Este objeto se recuperará automáticamente y se volverá a conectar a NapAgent, una vez que se reinicie.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

