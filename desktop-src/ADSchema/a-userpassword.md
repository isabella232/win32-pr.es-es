---
title: User-Password atributo)
description: Contraseña del usuario en formato UTF-8. Este atributo es de solo escritura.
ms.assetid: fcbd5e46-93fc-461e-aa6e-26d08114e73a
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de User-Password
- atributo userPassword esquema de AD
topic_type:
- apiref
api_name:
- User-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84dbb0b8bbc9ebf6995738050cddb226049658b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658718"
---
# <a name="user-password-attribute"></a>User-Password atributo)

Contraseña del usuario en formato UTF-8. Este atributo es de solo escritura.



| Entrada | Value |
|-------------------|-------------------------------------------------------|
| CN                | User-Password                                         |
| Nombre para mostrar de LDAP | userPassword                                          |
| Tamaño              | \-                                                    |
| Actualizar privilegio  | Administrador de dominio o propietario de la cuenta.                |
| Frecuencia de actualización  | \-                                                    |
| Attribute-Id      | 2.5.4.35                                              |
| System-ID-GUID    | bf967a6e-0de6-11d0-a285-00aa003049e2                  |
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
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                     |
| MAPI-Id                | 0x8153                                                                                                                                                 |
| System-Only            | False                                                                                                                                                  |
| Tiene un único valor       | False                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                  |
| En el catálogo global      | False                                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                           |
| Range-Lower            | 1                                                                                                                                                      |
| Range-Upper            | 128                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                             |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                       |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                    |
| Tiene un único valor       | False                                                                                                                                                                                                                    |
| Está indexado             | False                                                                                                                                                                                                                    |
| En el catálogo global      | False                                                                                                                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                                                                                        |
| Range-Upper            | 128                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                                                                                               |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                               |
| MAPI-Id                | 0x8153                                                                                                           |
| System-Only            | False                                                                                                            |
| Tiene un único valor       | False                                                                                                            |
| Está indexado             | False                                                                                                            |
| En el catálogo global      | False                                                                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                        |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                        |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                        |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                        |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                        |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                        |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                        |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                        |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                        |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                        |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                        |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                        |
| En el catálogo global      | False                                                                                                                                                                                                                                                                                                                                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



 

 





