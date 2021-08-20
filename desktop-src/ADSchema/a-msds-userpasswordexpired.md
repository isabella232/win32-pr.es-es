---
title: Atributo ms-DS-User-Password-Expired
description: Indica si la contraseña de la cuenta a la que hace referencia este atributo ha expirado.
ms.assetid: cab4a2e8-b440-45d2-8da8-9f020ffee08c
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DS-User-Password-Expired
- Esquema de AD del atributo msDS-UserPasswordExpired
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Expired
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a187f9d0b2be2feeca076d7c7eef82a34ca5827a9d07c76b2d711a5196f84ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425361"
---
# <a name="ms-ds-user-password-expired-attribute"></a>Atributo ms-DS-User-Password-Expired

Indica si la contraseña de la cuenta a la que hace referencia este atributo ha expirado. True si la contraseña ha expirado; de lo contrario, False.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Password-Expired          |
| Ldap-Display-Name | msDS-UserPasswordExpired             |
| Size              | \-                                   |
| Actualizar privilegios  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1858              |
| System-Id-Guid    | 565c7ab5-e13e-47f6-abb5-de741806f125 |
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
| System-Flags           | 0x00000014                                                        |
| Clases usadas en        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Comentarios

En ADAM, este atributo reemplaza la marca [**ADS \_ UF \_ PASSWORD \_ EXPIRED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) del [**atributo userAccountControl.**](a-useraccountcontrol.md)

 

