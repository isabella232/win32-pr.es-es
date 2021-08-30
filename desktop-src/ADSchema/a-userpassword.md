---
title: User-Password atributo
description: Contraseña del usuario en formato UTF-8. Se trata de un atributo de solo escritura.
ms.assetid: fcbd5e46-93fc-461e-aa6e-26d08114e73a
ms.tgt_platform: multiple
keywords:
- User-Password esquema de AD del atributo
- Esquema de AD del atributo userPassword
topic_type:
- apiref
api_name:
- User-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d15fae037e2b2e8fdb7889b6ba18e0269244174a80f7a373edc2b1457faced1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922925"
---
# <a name="user-password-attribute"></a>User-Password atributo

Contraseña del usuario en formato UTF-8. Se trata de un atributo de solo escritura.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | User-Password                                         |
| Ldap-Display-Name | Contraseña_usuario                                          |
| Size              | \-                                                    |
| Privilegio actualizar  | Administrador de dominio o propietario de la cuenta.                |
| Frecuencia de actualización  | \-                                                    |
| Attribute-Id      | 2.5.4.35                                              |
| System-Id-Guid    | bf967a6e-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                     |
| MAPI-Id                | 0x8153                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                  |
| Es de un solo valor       | Falso                                                                                                                                                  |
| Está indexado             | Falso                                                                                                                                                  |
| En el catálogo global      | Falso                                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                           |
| Range-Lower            | 1                                                                                                                                                      |
| Range-Upper            | 128                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                             |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                       |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                    |
| Es de un solo valor       | Falso                                                                                                                                                                                                                    |
| Está indexado             | Falso                                                                                                                                                                                                                    |
| En el catálogo global      | Falso                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                                                                                        |
| Range-Upper            | 128                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                                                                                               |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                               |
| MAPI-Id                | 0x8153                                                                                                           |
| System-Only            | Falso                                                                                                            |
| Es de un solo valor       | Falso                                                                                                            |
| Está indexado             | Falso                                                                                                            |
| En el catálogo global      | Falso                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



 

 





