---
title: Método INapSystemHealthValidationRequest GetStringCorrelationId (NapSystemHealthValidator.h)
description: Lo usan los validadores de estado del sistema (SHV), que deben registrar esta información.
ms.assetid: c3e45857-463b-4048-a178-ec26a318b63b
keywords:
- Método NAP de GetStringCorrelationId
- Método NAP de GetStringCorrelationId , interfaz INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP , GetStringCorrelationId method
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetStringCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 554a5a31f0aa46f6bcbd7a750662d47ab2c78040
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161283"
---
# <a name="inapsystemhealthvalidationrequestgetstringcorrelationid-method"></a>INapSystemHealthValidationRequest::GetStringCorrelationId (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de estado del sistema (SHV) que deben registrar esta información usan el método **INapSystemHealthValidationRequest::GetStringCorrelationId.**

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

Puntero a un puntero a un [**stringCorrelationId único**](nap-type-constants.md) para el intercambio soH.

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
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





