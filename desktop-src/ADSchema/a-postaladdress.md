---
title: Postal-Address atributo)
description: Dirección de correo para el objeto.
ms.assetid: 85e96b88-8e58-4916-a333-59e3d4ed8025
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Postal-Address
- postalAddress esquema de AD de atributos
topic_type:
- apiref
api_name:
- Postal-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c20616668546ae47af83620000495e482e5b778
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905937"
---
# <a name="postal-address-attribute"></a>Postal-Address atributo)

Dirección de correo para el objeto.



| Entrada | Value |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Postal-Address                                                              |
| Nombre para mostrar de LDAP | postalAddress                                                               |
| Tamaño              | \-                                                                          |
| Actualizar privilegio  | Administrador de dominio o propietario de la cuenta.                                      |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que se debe cambiar la dirección. |
| Attribute-Id      | 2.5.4.16                                                                    |
| System-ID-GUID    | bf9679fc-0de6-11d0-a285-00aa003049e2                                        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                 |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                          |
| System-Only            | False                                                                                                                                                                                                                                                                                                           |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                           |
| Está indexado             | False                                                                                                                                                                                                                                                                                                           |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                            |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                               |
| MAPI-Id                | 0x810C                                                                                                           |
| System-Only            | False                                                                                                            |
| Tiene un único valor       | False                                                                                                            |
| Está indexado             | False                                                                                                            |
| En el catálogo global      | False                                                                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 4096                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





