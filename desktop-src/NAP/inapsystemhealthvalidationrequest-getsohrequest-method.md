---
title: Método INapSystemHealthValidationRequest GetSoHRequest (NapSystemHealthValidator. h)
description: Permite que los validadores de mantenimiento del sistema (SHV) recuperen y validen la información SoHRequest enviada por sus homólogos del agente de mantenimiento del sistema (SHA) en el cliente.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interfaz INapSystemHealthValidationRequest
- Interfaz INapSystemHealthValidationRequest NAP, método GetSoHRequest
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
ms.openlocfilehash: 306c9307f99f91e0b0a48a1c5ffeaf19b4ea1f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151198"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a>INapSystemHealthValidationRequest:: GetSoHRequest (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSystemHealthValidationRequest:: GetSoHRequest** permite que los validadores de mantenimiento del sistema (SHV) recuperen y validen la información de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) enviada por sus homólogos del agente de mantenimiento del sistema (SHA) en el cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohRequest* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*napSystemGenerated* \[ enuncia\]
</dt> <dd>

Valor **booleano** que es **true** si el SOH lo creó NAPAGENT en nombre de Sha y **false** en caso contrario. Se utiliza principalmente para indicar un error SHA en el SHV.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

El parámetro *sohRequest* puede devolver **null** si el cliente no envió un [**sohRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) al SHV. En ese escenario, el SHV puede rellenar un **SoHResponse** con el código de error del [**\_ \_ \_ SOH que falta de NAP E**](nap-error-constants.md).

Si el parámetro *napSystemGenerated* es **true**, el formato de *SoHRequest* es el siguiente:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **<Sha-error-código>**](nap-error-constants.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





