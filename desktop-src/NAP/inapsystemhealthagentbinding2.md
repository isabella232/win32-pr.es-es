---
title: Interfaz INapSystemHealthAgentBinding2 (NapSystemHealthAgent.h)
description: Los SHA usan para comunicarse con NapAgent. | Interfaz INapSystemHealthAgentBinding2 (NapSystemHealthAgent.h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- NAP de interfaz INapSystemHealthAgentBinding2
- Interfaz NAP de INapSystemHealthAgentBinding2 , descrita
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a7491a2e78d66399f9ca246bcee9182e4f95d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071649"
---
# <a name="inapsystemhealthagentbinding2-interface"></a>Interfaz INapSystemHealthAgentBinding2

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapSystemHealthAgentBinding2 proporciona métodos** que los SHA usan para comunicarse con NapAgent.

> [!Note]  
> Esta interfaz hereda todos los métodos de [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) y se debe usar en su lugar.

 

## <a name="members"></a>Members

La **interfaz INapSystemHealthAgentBinding2** hereda de [**INapSystemHealthAgentBinding.**](inapsystemhealthagentbinding.md) **INapSystemHealthAgentBinding2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapSystemHealthAgentBinding2** tiene estos métodos.



| Método                                                                                                                    | Descripción                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | Lo llaman los SHA para determinar el estado de aislamiento del sistema y el estado de aislamiento extendido.<br/> |



 

## <a name="remarks"></a>Observaciones

Todas las API de esta interfaz **devolverán RPC \_ E \_ DISCONNECTED** si napagent está detenido. Este objeto se recuperará automáticamente y se volverá a conectar a NapAgent, una vez que se reinicie.

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

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

 





