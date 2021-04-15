---
title: Interfaz INapSystemHealthValidationRequest2 (NapSystemHealthValidator. h)
description: Proporciona métodos que se usan para admitir validadores de mantenimiento del sistema definidos por el desarrollador de la aplicación.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- Interfaz INapSystemHealthValidationRequest2 NAP
- Interfaz INapSystemHealthValidationRequest2 NAP, descripción
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677007"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a>Interfaz INapSystemHealthValidationRequest2

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La interfaz **INapSystemHealthValidationRequest2** proporciona métodos que se usan para admitir los validadores de mantenimiento del sistema definidos por el desarrollador de la aplicación.

> [!Note]  
> Esta interfaz hereda todos los métodos de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) y se debe usar en su lugar.

 

## <a name="members"></a>Miembros

La interfaz **INapSystemHealthValidationRequest2** hereda de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md). **INapSystemHealthValidationRequest2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapSystemHealthValidationRequest2** tiene estos métodos.



| Método                                                                                                    | Descripción                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest2::GetConfigId**](inapsystemhealthvalidationrequest2-getconfigid.md) | Recupera el identificador de configuración en una solicitud de validación.<br/> |



 

## <a name="remarks"></a>Observaciones

Si un SHV no es compatible con [**INapComponentConfig3**](inapcomponentconfig3.md), esta interfaz no se aplica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

 





