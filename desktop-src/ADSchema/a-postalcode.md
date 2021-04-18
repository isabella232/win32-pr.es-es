---
title: Postal-Code atributo)
description: Código postal o postal para la entrega de correo.
ms.assetid: bc8c4f52-df95-4676-beee-e6b86ba668a9
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Postal-Code
- Esquema de AD del atributo CódPostal
topic_type:
- apiref
api_name:
- Postal-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284295797c3ca5449fad72a834bd46c460b51cb7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658486"
---
# <a name="postal-code-attribute"></a>Postal-Code atributo)

Código postal o postal para la entrega de correo.



| Entrada | Value |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Postal-Code                                                                 |
| Nombre para mostrar de LDAP | postalCode                                                                  |
| Tamaño              | \-                                                                          |
| Actualizar privilegio  | Administrador de dominio o propietario de la cuenta.                                      |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que se debe cambiar la dirección. |
| Attribute-Id      | 2.5.4.17                                                                    |
| System-ID-GUID    | bf9679fd-0de6-11d0-a285-00aa003049e2                                        |
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
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                          |
| System-Only            | False                                                                                                                                                                                                                                                                                                           |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                            |
| Está indexado             | False                                                                                                                                                                                                                                                                                                           |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                                    |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                               |
| MAPI-Id                | 0x3A2A                                                                                                           |
| System-Only            | False                                                                                                            |
| Tiene un único valor       | True                                                                                                             |
| Está indexado             | False                                                                                                            |
| En el catálogo global      | False                                                                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 40                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                                    |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                                    |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                                    |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                                    |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





