---
title: Método INapSystemHealthValidationRequest GetSoHRequest (NapSystemHealthValidator.h)
description: Permite a los validadores de estado del sistema (SHV) recuperar y validar la información de SoHRequest enviada por sus homólogos del Agente de mantenimiento del sistema (SHA) en el cliente.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- Método NAP de GetSoHRequest
- Método NAP de GetSoHRequest, interfaz INapSystemHealthValidationRequest
- Interfaz NAP de INapSystemHealthValidationRequest, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9c140af202de263e99f0fa8ec72186da6e995ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161290"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a>INapSystemHealthValidationRequest::GetSoHRequest (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSystemHealthValidationRequest::GetSoHRequest** permite a los validadores de estado del sistema (SHV) recuperar y validar la información [**de SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) enviada por sus homólogos de System Health Agent (SHA) en el cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohRequest* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura SoHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> <dt>

*napSystemGenerated* \[ out\]
</dt> <dd>

Un **VALOR BOOL** que es **TRUE** si NapAgent creó el SoH en nombre de SHA y **FALSE** en caso contrario. Se usa principalmente para indicar un error sha en la SHV.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

El *parámetro sohRequest* puede devolver **NULL** si el cliente no envió [**un SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a shv. En ese escenario, shv puede rellenar un **SoHResponse** con el código de error [**de NAP E MISSING \_ \_ \_ SOH**](nap-error-constants.md).

Si el *parámetro napSystemGenerated* es **TRUE,** el formato *de SoHRequest* es el siguiente:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) =  &lt; Id&gt;
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **&lt; &gt; sha-failure-error-error-code**](nap-error-constants.md)

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

 

 





