---
title: atributo MS-DS-usuario-cifrado-texto-contraseña permitido
description: Indica si Active Directory almacenará la contraseña en el formato de cifrado reversible.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- 'MS-DS-User-Encrypted-Text-Password: esquema de AD de atributos permitidos'
- Esquema de AD del atributo MS-DS-UserEncryptedTextPasswordAllowed
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493570"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a>atributo MS-DS-usuario-cifrado-texto-contraseña permitido

Indica si Active Directory almacenará la contraseña en el formato de cifrado reversible. True si la contraseña se almacena en el formato de cifrado reversible; en caso contrario, false.

> [!Note]  
> [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) no utiliza este atributo y solo se incluye para la integridad o la paridad con UserAccountControl. AD LDS no almacena contraseñas con cifrado reversible, independientemente del valor de este atributo en un objeto determinado o en la Directiva de seguridad del equipo que pertenece al cifrado reversible en el propio equipo.

 



| Entrada | Value |
|-------------------|--------------------------------------------|
| CN                | MS-DS-usuario-cifrado-texto-contraseña-permitido |
| Nombre para mostrar de LDAP | MS-DS-UserEncryptedTextPasswordAllowed     |
| Tamaño              | \-                                         |
| Actualizar privilegio  | \-                                         |
| Frecuencia de actualización  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.1856                    |
| System-ID-GUID    | 5a87c7f2-93c5-454c-a8c5-8cb09613292e       |
| Sintaxis            | [**Booleano**](s-boolean.md)               |



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

En ADAM, este atributo reemplaza la marca de la [**\_ contraseña de \_ texto cifrado de ad fi \_ \_ \_ permitida**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) del atributo [**UserAccountControl**](a-useraccountcontrol.md) .

 

