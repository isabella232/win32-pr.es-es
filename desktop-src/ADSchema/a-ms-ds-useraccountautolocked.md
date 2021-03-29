---
title: atributo MS-DS-User-Account-auto-Locked
description: Indica si la cuenta a la que este atributo hace referencia se ha bloqueado.
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-User-Account-auto-Locked
- Esquema de AD del atributo MS-DS-UserAccountAutoLocked
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6623a1b348af14fecc8dab41a44439bf2d745bf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104079860"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a>atributo MS-DS-User-Account-auto-Locked

Indica si la cuenta a la que este atributo hace referencia se ha bloqueado. True si la cuenta está bloqueada; en caso contrario, false.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | MS-DS-usuario-cuenta-bloqueo automático       |
| Nombre para mostrar de LDAP | MS-DS-UserAccountAutoLocked          |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1857              |
| System-ID-GUID    | f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d |
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
| System-Flags           | 0x00000014                                                        |
| Clases usadas en        | [**Objeto MS-DS-Bindable**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Observaciones

En ADAM, este atributo reemplaza la marca de [**\_ \_ bloqueo de ad up**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) del atributo [**UserAccountControl**](a-useraccountcontrol.md) .

 

