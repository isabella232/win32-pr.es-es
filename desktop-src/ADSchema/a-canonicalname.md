---
title: Canonical-Name atributo
description: Nombre del objeto en formato canónico.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Canonical-Name esquema de AD del atributo
- Esquema de AD del atributo canonicalName
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d88b31dd351e255c252188388bd1ba06b3a1c073163f5cd2cc9d2deac16a74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119307195"
---
# <a name="canonical-name-attribute"></a>Canonical-Name atributo

Nombre del objeto en formato canónico. myserver2.fabrikam.com/users/jeffsmith es un ejemplo de un nombre distintivo en formato canónico. Se trata de un atributo construido. Los resultados devueltos son idénticos a los devueltos por la siguiente función Active Directory: DsCrackNames(NULL, DS \_ NAME \_ FLAG \_ SYNTACTICAL \_ ONLY, DS \_ FQDN \_ 1779 \_ NAME, DS \_ CANONICAL \_ NAME, ...).

Para obtener más información sobre los formatos de nombre, [**vea DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Canonical-Name                              |
| Ldap-Display-Name | canonicalName                               |
| Size              | \-                                          |
| Privilegio actualizar  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.916                      |
| System-Id-Guid    | 9a7ad945-ca53-11d1-bbd0-0080c76670c0        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Es de un solo valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Es de un solo valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Es de un solo valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Es de un solo valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Es de un solo valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Es de un solo valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Es de un solo valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



 

