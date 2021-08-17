---
title: Telephone-Number atributo
description: Número de teléfono principal.
ms.assetid: 6a7faad4-9d86-4821-9b00-67adbf1b05f2
ms.tgt_platform: multiple
keywords:
- Telephone-Number esquema de AD del atributo
- Esquema de AD del atributo telephoneNumber
topic_type:
- apiref
api_name:
- Telephone-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d86054b50ae511b3f519c1c289fb529eaa8a2e7279adb7b66cbfc2df32c3758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923125"
---
# <a name="telephone-number-attribute"></a>Telephone-Number atributo

Número de teléfono principal.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Telephone-Number                                                                 |
| Ldap-Display-Name | telephoneNumber                                                                  |
| Size              | \-                                                                               |
| Privilegio actualizar  | Cualquier persona puede actualizar este objeto en función de la seguridad del objeto que se va a crear. |
| Frecuencia de actualización  | \-                                                                               |
| Attribute-Id      | 2.5.4.20                                                                         |
| System-Id-Guid    | bf967a49-0de6-11d0-a285-00aa003049e2                                             |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Destinatario del correo**](c-mailrecipient.md)<br/> [**Organización**](c-organization.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/> [**Organización**](c-organization.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Habitación**](c-room.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                               |
| MAPI-Id                | 0x3A08                                                                                                           |
| System-Only            | Falso                                                                                                            |
| Es de un solo valor       | Verdadero                                                                                                             |
| Está indexado             | Falso                                                                                                            |
| En el catálogo global      | Verdadero                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 64                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/> [**Organización**](c-organization.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Habitación**](c-room.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/> [**Organización**](c-organization.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Habitación**](c-room.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**Organización**](c-organization.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Habitación**](c-room.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**Organización**](c-organization.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Habitación**](c-room.md)<br/> |



 

 





