---
title: Interfaz INapSystemHealthAgentRequest (NapSystemHealthAgent.h)
description: Las SHA usan para comunicar y coordinar el procesamiento con el sistema NAP.
ms.assetid: 424e0fb7-cce7-4b75-b474-fda0e053284e
keywords:
- Interfaz NAP de INapSystemHealthAgentRequest
- Interfaz NAP de INapSystemHealthAgentRequest , descrita
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e79e2a6347ebffec37595d4ca86b100830047
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161296"
---
# <a name="inapsystemhealthagentrequest-interface"></a>INapSystemHealthAgentRequest (interfaz)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **interfaz INapSystemHealthAgentRequest proporciona** métodos que las SHA usan para comunicar y coordinar el procesamiento con el sistema NAP.

## <a name="members"></a>Members

La **interfaz INapSystemHealthAgentRequest** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthAgentRequest** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapSystemHealthAgentRequest** tiene estos métodos.



| Método                                                                                                                     | Descripción                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentRequest::GetCacheSoHFlag**](inapsystemhealthagentrequest-getcachesohflag-method.md)               | Solo lo usa NapAgent.<br/>                                                            |
| [**INapSystemHealthAgentRequest::GetCorrelationId**](inapsystemhealthagentrequest-getcorrelationid-method.md)             | Lo usan los agentes de mantenimiento del sistema para correlacionar SoHs y [**SoHResponse.**](/windows/win32/api/naptypes/ns-naptypes-soh)<br/> |
| [**INapSystemHealthAgentRequest::GetSoHRequest**](inapsystemhealthagentrequest-getsohrequest-method.md)                   | Lo usan las SHA para obtener los SOH previamente almacenados en caché por NapAgent.<br/>                           |
| [**INapSystemHealthAgentRequest::GetSoHResponse**](inapsystemhealthagentrequest-getsohresponse-method.md)                 | Usado por el agente de mantenimiento para recuperar su [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).<br/>         |
| [**INapSystemHealthAgentRequest::GetStringCorrelationId**](inapsystemhealthagentrequest-getstringcorrelationid-method.md) | Lo usan los agentes de mantenimiento del sistema para registrar el identificador de correlación.<br/>                               |
| [**INapSystemHealthAgentRequest::SetSoHRequest**](inapsystemhealthagentrequest-setsohrequest-method.md)                   | Lo usan los agentes de mantenimiento para escribir su solicitud de SoH.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

