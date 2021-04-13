---
title: Método INapSystemHealthAgentRequest GetCorrelationId (NapSystemHealthAgent. h)
description: Lo utilizan los agentes de mantenimiento del sistema para correlacionar las respuestas de SoH y SoH.
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- Método GetCorrelationId NAP
- Método GetCorrelationId NAP, interfaz INapSystemHealthAgentRequest
- Interfaz INapSystemHealthAgentRequest NAP, método GetCorrelationId
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
ms.openlocfilehash: 7af5b182df738ec22c75f2afffd1adb3591007be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535602"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a>INapSystemHealthAgentRequest:: GetCorrelationId (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los agentes de mantenimiento del sistema usan el método **INapSystemHealthAgentRequest:: GetCorrelationId** para correlacionar las respuestas del SOH y el SOH.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CorrelationId* \[ enuncia\]
</dt> <dd>

Un puntero a un [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) único para el intercambio de SOH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





