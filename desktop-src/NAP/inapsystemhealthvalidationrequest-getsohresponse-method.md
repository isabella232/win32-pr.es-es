---
title: Método INapSystemHealthValidationRequest GetSoHResponse (NapSystemHealthValidator.h)
description: Recupera soHResponse.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- Método NAP de GetSoHResponse
- Método NAP de GetSoHResponse, interfaz INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP , GetSoHResponse method
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da93f53f3dcc9f4e566703d4d2f63415bb7feb9b0c00d5086fe598ab442e1d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799062"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a>Método INapSystemHealthValidationRequest::GetSoHResponse

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSystemHealthValidationRequest::GetSoHResponse** recupera [**soHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohResponse* \[ out\]
</dt> <dd>

Puntero a un puntero al objeto [**SoHResponse recibido.**](/windows/win32/api/naptypes/ns-naptypes-soh)

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
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





