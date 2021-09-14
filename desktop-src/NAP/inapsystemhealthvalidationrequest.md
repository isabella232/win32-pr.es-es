---
title: Interfaz INapSystemHealthValidationRequest (NapSystemHealthValidator.h)
description: Se usan para admitir validadores de estado del sistema definidos por el desarrollador de aplicaciones.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- INapSystemHealthValidationRequest interface NAP
- Interfaz NAP INapSystemHealthValidationRequest , descrita
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf09f93e00401251a3d0e2296323edeb84ad6007
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161278"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a>INapSystemHealthValidationRequest (interfaz)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **interfaz INapSystemHealthValidationRequest** proporciona métodos que se usan para admitir validadores de estado del sistema definidos por el desarrollador de la aplicación.

> [!Note]  
> [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) hereda todos los métodos de esta interfaz y se debe usar en su lugar.

 

## <a name="members"></a>Members

La **interfaz INapSystemHealthValidationRequest** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthValidationRequest** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapSystemHealthValidationRequest** tiene estos métodos.



| Método                                                                                                                               | Descripción                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest::GetCorrelationId**](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | Lo usan los validadores para recuperar el identificador de correlación. A continuación, el validador debe registrar esta información.<br/>           |
| [**INapSystemHealthValidationRequest::GetMachineName**](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | Lo usan los validadores para recuperar el nombre de la máquina. A continuación, el validador debe registrar esta información.<br/>             |
| [**INapSystemHealthValidationRequest::GetPrivateData**](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | Permite que NapServer recupere información de estado.<br/>                                                        |
| [**INapSystemHealthValidationRequest::GetSoHRequest**](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | Permite a los validadores recuperar y validar la información de SoHRequest.<br/>                                     |
| [**INapSystemHealthValidationRequest::GetSoHResponse**](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | Obtiene el objeto SoHResponse.<br/>                                                                               |
| [**INapSystemHealthValidationRequest::GetStringCorrelationId**](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | Lo usan los validadores para recuperar un identificador de intercambio único. A continuación, el validador debe registrar esta información.<br/> |
| [**INapSystemHealthValidationRequest::SetPrivateData**](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | Permite que NapServer almacene información de estado.<br/>                                                           |
| [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | Permite que los validadores establezcan SoHResponse.<br/>                                                                  |



 

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

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

