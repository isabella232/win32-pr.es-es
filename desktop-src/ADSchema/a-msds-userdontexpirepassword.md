---
title: atributo de contraseña MS-DS-usuario-no-expiren
description: Indica si la contraseña de la cuenta a la que hacen referencia este atributo expirará.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de contraseña MS-DS-usuario-no-expiren
- Esquema de AD de atributo msDS-UserDontExpirePassword
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5c0fa709f549a523d628433ee2b3aa626278e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151648"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a>atributo de contraseña MS-DS-usuario-no-expiren

Indica si la contraseña de la cuenta a la que hacen referencia este atributo expirará. True si la contraseña no va a expirar; en caso contrario, false.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | MS-DS-usuario-no-expire-contraseña      |
| Nombre para mostrar de LDAP | msDS-UserDontExpirePassword          |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1855              |
| System-ID-GUID    | 8788193a-2925-43d9-a221-bb7fff397675 |
| Sintaxis            | [**Booleano**](s-boolean.md)         |



## <a name="implementations"></a>Implementaciones

-   [**ADAM**](#adam)

## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Tiene un único valor       | True                                                              |
| Está indexado             | False                                                             |
| En el catálogo global      | False                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Clases usadas en        | [**Objeto MS-DS-Bindable**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Observaciones

En ADAM, este atributo reemplaza la marca de la [**\_ \_ \_ \_ passwd ad fi no expire**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) en el atributo [**UserAccountControl**](a-useraccountcontrol.md) .

 

