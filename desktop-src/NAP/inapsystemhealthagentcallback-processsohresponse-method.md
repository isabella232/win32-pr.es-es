---
title: Método INapSystemHealthAgentCallback ProcessSoHResponse (NapSystemHealthAgent.h)
description: Se llama a cuando NapAgent recibe un SoHResponse destinado a este agente de mantenimiento.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- Método NAP de ProcessSoHResponse
- Método NAP de ProcessSoHResponse, interfaz INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP , ProcessSoHResponse method
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f5aaca7833560dbb53422da08ced158bb172610c3bacef931866d74d416fcce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367760"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a>Método INapSystemHealthAgentCallback::P rocessSoHResponse

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Se llama al método **INapSystemHealthAgentCallback::P rocessSoHResponse** cuando NapAgent recibe un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado a este agente de mantenimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*solicitud* \[ En\]
</dt> <dd>

Puntero COM a un [**objeto INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) que identifica el objeto de solicitud.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                            | Descripción                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Indica que se completó correctamente.<br/>                                                            |
| <dl> <dt>**PAQUETE NAP \_ E \_ NO \_ VÁLIDO**</dt> </dl> | Devuelto por esta implementación si la respuesta no tiene el formato correcto.<br/> |



 

## <a name="remarks"></a>Comentarios

El sistema NAP declara este método de devolución de llamada y lo va a implementar el escritor SHA.

Cuando NapAgent recibe un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado a este agente de mantenimiento, invoca este método. El agente de mantenimiento debe consultar SoHResponse desde el objeto de solicitud. No debe contener referencias al objeto de solicitud una vez completada esta llamada.

El **método INapSystemHealthAgentCallback::P rocessSoHResponse** no debe bloquearse. Si se requiere algún procesamiento de corrección, cualquier implementación de **ProcessSoHResponse** debe iniciar un nuevo subproceso para realizar el procesamiento de la corrección. NapAgent debe llamar a [**INapSystemHealthAgentCallBack::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) para determinar el estado de corrección de SHA.

Este método debe devolver **NAP \_ E INVALID \_ \_ PACKET** si la respuesta no tiene el formato correcto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





