---
title: Atributo State-Or-Province-Name
description: Nombre del estado o provincia de un usuario.
ms.assetid: 2096318e-29bf-4021-a422-371835f3a62b
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo State-Or-Province-Name
- Esquema de AD de atributo st
topic_type:
- apiref
api_name:
- State-Or-Province-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c818eb0a885d598edc10b5857aee23e336095c301d3b1059b25ba7b2f9fd986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959994"
---
# <a name="state-or-province-name-attribute"></a>Atributo State-Or-Province-Name

Nombre del estado o provincia de un usuario.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------------|
| CN                | State-Or-Province-Name                                                           |
| Ldap-Display-Name | st                                                                               |
| Size              | \-                                                                               |
| Actualizar privilegios  | Cualquiera puede actualizar este objeto en función de la seguridad del objeto que se va a crear. |
| Frecuencia de actualización  | \-                                                                               |
| Attribute-Id      | 2.5.4.8                                                                          |
| System-Id-Guid    | bf967a39-0de6-11d0-a285-00aa003049e2                                             |
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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                         |
| MAPI-Id                | 0x3A28                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                          |
| Range-Upper            | 128                                                                                                                                                        |
| Search-Flags           | 0x00000010                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                 |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> |



 

 





