---
title: Registered-Address atributo)
description: Especifica un mnemotécnico para una dirección asociada a un objeto en una ubicación de ciudad determinada. El mnemotécnico se registra en el país o región en el que se encuentra la ciudad y se usa en el aprovisionamiento del servicio de telegrama público.
ms.assetid: 5bc1eecd-0263-46da-a842-75ee94f77b58
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Registered-Address
- registeredAddress esquema de AD de atributos
topic_type:
- apiref
api_name:
- Registered-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a24093e8ebfa0edd5a2e2101f6da86cd6cd19d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658991"
---
# <a name="registered-address-attribute"></a>Registered-Address atributo)

Especifica un mnemotécnico para una dirección asociada a un objeto en una ubicación de ciudad determinada. El mnemotécnico se registra en el país o región en el que se encuentra la ciudad y se usa en el aprovisionamiento del servicio de telegrama público.



| Entrada | Value |
|-------------------|-------------------------------------------------------|
| CN                | Registered-Address                                    |
| Nombre para mostrar de LDAP | registeredAddress                                     |
| Tamaño              | \-                                                    |
| Actualizar privilegio  | \-                                                    |
| Frecuencia de actualización  | \-                                                    |
| Attribute-Id      | 2.5.4.26                                              |
| System-ID-GUID    | bf967a10-0de6-11d0-a285-00aa003049e2                  |
| Sintaxis            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                          |
| System-Only            | False                                                                                                                                                                                                                                                                                                           |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                           |
| Está indexado             | False                                                                                                                                                                                                                                                                                                           |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                               |
| MAPI-Id                | 0x8119                                                                                                           |
| System-Only            | False                                                                                                            |
| Tiene un único valor       | False                                                                                                            |
| Está indexado             | False                                                                                                            |
| En el catálogo global      | False                                                                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 4096                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000000                                                                                                       |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                   |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol de la organización**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





