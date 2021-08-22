---
title: Atributo ms-DS-User-Account-Auto-Locked
description: Indica si la cuenta a la que hace referencia este atributo se ha bloqueado.
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- ms-DS-User-Account-Auto-Locked attribute AD Schema
- Esquema de AD del atributo ms-DS-UserAccountAutoLocked
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1360b9169d5355ef23caf47fa56a283dc4e5267fb603aa08bd0600f126c69f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119300305"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a>Atributo ms-DS-User-Account-Auto-Locked

Indica si la cuenta a la que hace referencia este atributo se ha bloqueado. True si la cuenta está bloqueada; de lo contrario, False.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Auto-Locked       |
| Ldap-Display-Name | ms-DS-UserAccountAutoLocked          |
| Size              | \-                                   |
| Actualizar privilegios  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1857              |
| System-Id-Guid    | f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d |
| Syntax            | [**Booleana**](s-boolean.md)         |



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

En ADAM, este atributo reemplaza la marca [**ADS \_ UF \_ LOCKOUT**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) del [**atributo userAccountControl.**](a-useraccountcontrol.md)

 

