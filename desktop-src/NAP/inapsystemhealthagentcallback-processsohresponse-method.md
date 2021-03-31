---
title: Método INapSystemHealthAgentCallback ProcessSoHResponse (NapSystemHealthAgent. h)
description: Se llama a cuando el NapAgent recibe un SoHResponse destinado a este agente de mantenimiento.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- Método ProcessSoHResponse NAP
- Método ProcessSoHResponse NAP, interfaz INapSystemHealthAgentCallback
- Interfaz INapSystemHealthAgentCallback NAP, método ProcessSoHResponse
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
ms.openlocfilehash: 95c62c585c36680dde2c54c95c255a85f69fc5ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996532"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a>INapSystemHealthAgentCallback::P método rocessSoHResponse

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Se llama al método **INapSystemHealthAgentCallback::P rocesssohresponse** cuando NapAgent recibe un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado a este agente de mantenimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*solicitud* \[ de de\]
</dt> <dd>

Puntero COM a un objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) que identifica el objeto de solicitud.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                            | Descripción                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Indica que se completó correctamente.<br/>                                                            |
| <dl> <dt>**\_paquete NAP E \_ no válido \_**</dt> </dl> | Lo devuelve esta implementación si la respuesta no tiene el formato correcto.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método de devolución de llamada lo declara el sistema NAP y se va a implementar con SHA Writer.

Cuando el NapAgent recibe un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado a este agente de mantenimiento, invoca este método. El agente de mantenimiento debe consultar el SoHResponse desde el objeto de solicitud. No debe contener referencias al objeto de solicitud una vez completada esta llamada.

El método **INapSystemHealthAgentCallback::P rocesssohresponse** no debe bloquearse. Si se requiere un procesamiento de correcciones, cualquier implementación de **ProcessSoHResponse** debe iniciar un nuevo subproceso para realizar el procesamiento de la corrección. NapAgent debe llamar a [**INapSystemHealthAgentCallBack:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) para determinar el estado de corrección del Sha.

Este método debe devolver **el \_ paquete NAP E \_ no válido \_** si la respuesta no tiene el formato correcto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





