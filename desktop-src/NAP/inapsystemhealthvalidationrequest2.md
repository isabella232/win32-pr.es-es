---
title: Interfaz INapSystemHealthValidationRequest2 (NapSystemHealthValidator.h)
description: Proporciona métodos que se usan para admitir validadores de estado del sistema definidos por el desarrollador de aplicaciones.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- NAP de la interfaz INapSystemHealthValidationRequest2
- Interfaz NAP INapSystemHealthValidationRequest2 , descrita
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
ms.openlocfilehash: 2b6438394120ecd901c6de6d7a8ccac40f742d9f73d27a36682de894d9c5a7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620854"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a>Interfaz INapSystemHealthValidationRequest2

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **interfaz INapSystemHealthValidationRequest2** proporciona métodos que se usan para admitir validadores de estado del sistema definidos por el desarrollador de la aplicación.

> [!Note]  
> Esta interfaz hereda todos los métodos de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) y se debe usar en su lugar.

 

## <a name="members"></a>Miembros

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
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

 





