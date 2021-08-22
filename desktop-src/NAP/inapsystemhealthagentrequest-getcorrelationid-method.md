---
title: Método INapSystemHealthAgentRequest GetCorrelationId (NapSystemHealthAgent.h)
description: Lo usan los agentes de mantenimiento del sistema para correlacionar soH y soH-responses.
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- Método NAP de GetCorrelationId
- Método NAP de GetCorrelationId , interfaz INapSystemHealthAgentRequest
- Interfaz NAP de INapSystemHealthAgentRequest, método GetCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf02a6d72aaa2744cc5a1329d791bdb9e8fa31f7453b131268245e120d7087e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686165"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a>INapSystemHealthAgentRequest::GetCorrelationId (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los agentes de mantenimiento del sistema usan el método **INapSystemHealthAgentRequest::GetCorrelationId** para correlacionar soH y soH-responses.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*correlationId* \[ out\]
</dt> <dd>

Puntero a un [**correlationId único**](/windows/win32/api/naptypes/ns-naptypes-correlationid) para el intercambio de SoH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





