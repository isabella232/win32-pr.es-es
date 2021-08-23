---
title: Atributo ms-DS-User-Account-Disabled
description: Indica si una cuenta está habilitada o deshabilitada.
ms.assetid: 5d6ced7b-ca0f-4afa-b394-e61e80454f3d
ms.tgt_platform: multiple
keywords:
- ms-DS-User-Account-Disabled attribute AD Schema
- Esquema de AD del atributo msDS-UserAccountDisabled
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Disabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f0744cd835fab641de4f4d3386304a342fe3902fcf1a67b3367dc15b7ee68f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544145"
---
# <a name="ms-ds-user-account-disabled-attribute"></a>Atributo ms-DS-User-Account-Disabled

Indica si una cuenta está habilitada o deshabilitada. True si la cuenta está deshabilitada; de lo contrario, False.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Disabled          |
| Ldap-Display-Name | msDS-UserAccountDisabled             |
| Size              | \-                                   |
| Actualizar privilegios  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1853              |
| System-Id-Guid    | 7c708658-7372-4211-b22b-13a45ffd1d61 |
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

En ADAM, este atributo reemplaza la marca [**\_ \_ ACCOUNTDISABLE de ADS UF**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) del [**atributo userAccountControl.**](a-useraccountcontrol.md)

 

