---
title: Atributo ms-DS-User-Encrypted-Text-Password-Allowed
description: Indica si Active Directory almacenará la contraseña en el formato de cifrado reversible.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo ms-DS-User-Encrypted-Text-Password-Allowed
- ms-DS-UserEncryptedTextPasswordAllowed attribute AD Schema
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fc10b3facce4bef7cc5ff73abe9e901f67171dc2615b79c62355ac61a7c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118687006"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a>Atributo ms-DS-User-Encrypted-Text-Password-Allowed

Indica si Active Directory almacenará la contraseña en el formato de cifrado reversible. True si la contraseña se almacena en el formato de cifrado reversible; de lo contrario, False.

> [!Note]  
> Este atributo no se usa en [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) y solo se incluye por integridad o paridad con userAccountControl. AD LDS no almacena contraseñas con cifrado reversible, independientemente del valor de este atributo en cualquier objeto determinado o la directiva de seguridad del equipo relativa al cifrado reversible en el propio equipo.

 



| Entrada | Value |
|-------------------|--------------------------------------------|
| CN                | ms-DS-User-Encrypted-Text-Password-Allowed |
| Ldap-Display-Name | ms-DS-UserEncryptedTextPasswordAllowed     |
| Size              | \-                                         |
| Privilegio actualizar  | \-                                         |
| Frecuencia de actualización  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.1856                    |
| System-Id-Guid    | 5a87c7f2-93c5-454c-a8c5-8cb09613292e       |
| Sintaxis            | [**Booleana**](s-boolean.md)               |



## <a name="implementations"></a>Implementaciones

-   [**Adán**](#adam)

## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Es de un solo valor       | True                                                              |
| Está indexado             | False                                                             |
| En el catálogo global      | False                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Clases usadas en        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Observaciones

En ADAM, este atributo reemplaza la marca [**ADS \_ UF \_ ENCRYPTED TEXT \_ PASSWORD \_ \_ ALLOWED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) del [**atributo userAccountControl.**](a-useraccountcontrol.md)

 

