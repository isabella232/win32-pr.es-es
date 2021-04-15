---
title: atributo MS-DS-User-Account-Disabled
description: Indica si una cuenta está habilitada o deshabilitada.
ms.assetid: 5d6ced7b-ca0f-4afa-b394-e61e80454f3d
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo deshabilitado de la cuenta de usuario MS-DS-Account
- Esquema de AD de atributo msDS-UserAccountDisabled
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Disabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a01c0b83599a8d6309f6639b94f5d0321180df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494008"
---
# <a name="ms-ds-user-account-disabled-attribute"></a>atributo MS-DS-User-Account-Disabled

Indica si una cuenta está habilitada o deshabilitada. True si la cuenta está deshabilitada; en caso contrario, false.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | MS-DS-usuario-cuenta-deshabilitado          |
| Nombre para mostrar de LDAP | msDS-UserAccountDisabled             |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1853              |
| System-ID-GUID    | 7c708658-7372-4211-b22b-13a45ffd1d61 |
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

En ADAM, este atributo reemplaza la [**marca \_ ADS \_ ACCOUNTDISABLE**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) del atributo [**UserAccountControl**](a-useraccountcontrol.md) .

 

