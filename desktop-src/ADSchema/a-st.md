---
title: Atributo de nombre de estado o provincia
description: Nombre del estado o provincia de un usuario.
ms.assetid: 2096318e-29bf-4021-a422-371835f3a62b
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo de nombre de estado o provincia
- atributo St esquema AD
topic_type:
- apiref
api_name:
- State-Or-Province-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677daf6d72c63ffd08cc1ac8540e4ba03c3af792
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104079827"
---
# <a name="state-or-province-name-attribute"></a>Atributo de nombre de estado o provincia

Nombre del estado o provincia de un usuario.



| Entrada | Value |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Nombre de estado o provincia                                                           |
| Nombre para mostrar de LDAP | st                                                                               |
| Tamaño              | \-                                                                               |
| Actualizar privilegio  | Cualquier usuario puede actualizar este objeto en función de la seguridad del objeto que se va a crear. |
| Frecuencia de actualización  | \-                                                                               |
| Attribute-Id      | 2.5.4.8                                                                          |
| System-ID-GUID    | bf967a39-0de6-11d0-a285-00aa003049e2                                             |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                         |
| MAPI-Id                | 0x3A28                                                                                                                                                     |
| System-Only            | False                                                                                                                                                      |
| Tiene un único valor       | True                                                                                                                                                       |
| Está indexado             | False                                                                                                                                                      |
| En el catálogo global      | True                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                          |
| Range-Upper            | 128                                                                                                                                                        |
| Search-Flags           | 0x00000010                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                 |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                      |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                     |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



 

 





