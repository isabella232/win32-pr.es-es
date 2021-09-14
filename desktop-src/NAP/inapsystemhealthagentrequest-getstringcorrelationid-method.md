---
title: Método INapSystemHealthAgentRequest GetStringCorrelationId (NapSystemHealthAgent.h)
description: Los agentes de mantenimiento del sistema usan para registrar el identificador de correlación.
ms.assetid: 5d6f2392-2ada-474a-b150-31e0583c2ea7
keywords:
- Método NAP de GetStringCorrelationId
- Método NAP de GetStringCorrelationId , interfaz INapSystemHealthAgentRequest
- Interfaz NAP de INapSystemHealthAgentRequest, método GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetStringCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f33e98ae4b0fd76d97e85fb3588bcd1f2d33fd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161298"
---
# <a name="inapsystemhealthagentrequestgetstringcorrelationid-method"></a>INapSystemHealthAgentRequest::GetStringCorrelationId (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los agentes de mantenimiento del sistema usan el método **INapSystemHealthAgentRequest::GetStringCorrelationId** para registrar el identificador de correlación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*correlationId* \[ out\]
</dt> <dd>

Puntero a un puntero a un [**correlationId único**](/windows/win32/api/naptypes/ns-naptypes-correlationid) para este intercambio de SoH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

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

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





