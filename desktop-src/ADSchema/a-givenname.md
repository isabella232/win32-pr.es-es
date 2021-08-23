---
title: Given-Name atributo
description: Contiene el nombre especificado (nombre) del usuario.
ms.assetid: acffe751-9911-4e80-8a26-351a21a6385e
ms.tgt_platform: multiple
keywords:
- Given-Name esquema de AD de atributo
- Esquema de AD del atributo givenName
topic_type:
- apiref
api_name:
- Given-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ee788506d098123888a9389d9256dd4203cae463cf008723e99e8180750d591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706065"
---
# <a name="given-name-attribute"></a>Given-Name atributo

Contiene el nombre especificado (nombre) del usuario.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Given-Name                                  |
| Ldap-Display-Name | givenName                                   |
| Size              | \-                                          |
| Actualizar privilegios  | Administrador de dominio o propietario de la cuenta.      |
| Frecuencia de actualización  | Cuando se crea el registro del usuario.          |
| Attribute-Id      | 2.5.4.42                                    |
| System-Id-Guid    | f0f8ff8e-1191-11d0-a060-00aa006c33ed        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|--------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                 |
| MAPI-Id                | 0x3A06                                                             |
| System-Only            | Falso                                                              |
| Es de un solo valor       | Verdadero                                                               |
| Está indexado             | Verdadero                                                               |
| En el catálogo global      | Verdadero                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000005                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Es de un solo valor       | Verdadero                                                                                                                   |
| Está indexado             | Verdadero                                                                                                                   |
| En el catálogo global      | Verdadero                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Es de un solo valor       | Verdadero                                                                                                                   |
| Está indexado             | Verdadero                                                                                                                   |
| En el catálogo global      | Verdadero                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Es de un solo valor       | Verdadero                                                                                                                   |
| Está indexado             | Verdadero                                                                                                                   |
| En el catálogo global      | Verdadero                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Es de un solo valor       | Verdadero                                                                                                                   |
| Está indexado             | Verdadero                                                                                                                   |
| En el catálogo global      | Verdadero                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Es de un solo valor       | Verdadero                                                                                                                   |
| Está indexado             | Verdadero                                                                                                                   |
| En el catálogo global      | Verdadero                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





