---
title: Atributo ms-DS-User-Dont-Expire-Password
description: Indica si la contraseña de la cuenta a la que hace referencia este atributo expirará.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DS-User-Dont-Expire-Password
- Esquema de AD del atributo msDS-UserDontExpirePassword
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af661ca1317f7506e5bcdbf611010b0fe4c058d5f1e3f1e5f31b917737a6e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425435"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a>Atributo ms-DS-User-Dont-Expire-Password

Indica si la contraseña de la cuenta a la que hace referencia este atributo expirará. True si la contraseña no expirará; de lo contrario, False.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Dont-Expire-Password      |
| Ldap-Display-Name | msDS-UserDontExpirePassword          |
| Size              | \-                                   |
| Actualizar privilegios  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1855              |
| System-Id-Guid    | 8788193a-2925-43d9-a221-bb7fff397675 |
| Syntax            | [**Boolean**](s-boolean.md)         |



## <a name="implementations"></a>Implementaciones

-   [**Adán**](#adam)

## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Es de un solo valor       | Verdadero                                                              |
| Está indexado             | Falso                                                             |
| En el catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Clases usadas en        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Comentarios

En ADAM, este atributo reemplaza la marca PASSWD de [**ADS \_ UF \_ DONT \_ EXPIRE \_**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) del [**atributo userAccountControl.**](a-useraccountcontrol.md)

 

