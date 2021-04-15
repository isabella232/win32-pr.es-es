---
title: Interfaz INapSystemHealthAgentCallback (NapSystemHealthAgent. h)
description: Los declara el sistema e implementan el sistema de escritura SHA para que el NapAgent pueda comunicarse con el SHA.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- Interfaz INapSystemHealthAgentCallback NAP
- Interfaz INapSystemHealthAgentCallback NAP, descripción
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676885"
---
# <a name="inapsystemhealthagentcallback-interface"></a>Interfaz INapSystemHealthAgentCallback

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La interfaz **INapSystemHealthAgentCallback** proporciona métodos de devolución de llamada declarados por el sistema e implementados por el escritor Sha para que NapAgent pueda comunicarse con el Sha.

## <a name="members"></a>Miembros

La interfaz **INapSystemHealthAgentCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthAgentCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapSystemHealthAgentCallback** tiene estos métodos.



| Método                                                                                                                                           | Descripción                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentCallback::CompareSoHRequests**](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | Utilizado por SHA para comparar el SOH.<br/>                                                                      |
| [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | Lo llama NapAgent para determinar el estado del SHA.<br/>                                                 |
| [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | Llamado por el NapAgent para consultar la solicitud de SoH de SHA.<br/>                                                    |
| [**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | Se llama si se ha consultado una solicitud de SoH desde SHA, pero la respuesta nunca llegó.<br/>                      |
| [**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | Lo llama NapAgent para indicar que ha cambiado el estado de aislamiento del sistema o el tiempo de finalización del período de prueba.<br/> |
| [**INapSystemHealthAgentCallback::P rocessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md)                             | Se llama cuando NapAgent recibe una respuesta de SoH destinada a este agente de mantenimiento.<br/>                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

