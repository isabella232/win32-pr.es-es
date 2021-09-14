---
title: Interfaz INapSystemHealthValidationRequest2 (NapSystemHealthValidator.h)
description: Proporciona métodos que se usan para admitir validadores de estado del sistema definidos por el desarrollador de aplicaciones.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- NAP de la interfaz INapSystemHealthValidationRequest2
- Interfaz NAP de INapSystemHealthValidationRequest2 , descrita
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161275"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a>Interfaz INapSystemHealthValidationRequest2

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **interfaz INapSystemHealthValidationRequest2** proporciona métodos que se usan para admitir validadores de estado del sistema definidos por el desarrollador de la aplicación.

> [!Note]  
> Esta interfaz hereda todos los métodos de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) y se debe usar en su lugar.

 

## <a name="members"></a>Members

La **interfaz INapSystemHealthValidationRequest2** hereda de [**INapSystemHealthValidationRequest.**](inapsystemhealthvalidationrequest.md) **INapSystemHealthValidationRequest2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapSystemHealthValidationRequest2** tiene estos métodos.



| Método                                                                                                    | Descripción                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest2::GetConfigId**](inapsystemhealthvalidationrequest2-getconfigid.md) | Recupera el identificador de configuración en una solicitud de validación.<br/> |



 

## <a name="remarks"></a>Observaciones

Si una SHV no admite [**INapComponentConfig3,**](inapcomponentconfig3.md)esta interfaz no se aplica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

 





