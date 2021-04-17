---
title: 'Phone-Home: atributo principal'
description: Número de teléfono principal del usuario.
ms.assetid: 624d89fd-942c-448d-bd51-7d93954370b1
ms.tgt_platform: multiple
keywords:
- 'Phone-Home: esquema de AD de atributo principal'
- homePhone esquema de AD de atributos
topic_type:
- apiref
api_name:
- Phone-Home-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d2e68116a15dcbf4431d33bb56b4ffed8ee2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658957"
---
# <a name="phone-home-primary-attribute"></a>Phone-Home: atributo principal

Número de teléfono principal del usuario.



| Entrada | Value |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Teléfono-Inicio-principal                                                               |
| Nombre para mostrar de LDAP | homePhone                                                                        |
| Tamaño              | \-                                                                               |
| Actualizar privilegio  | Administrador de dominio o propietario de la cuenta.                                           |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que es necesario cambiar el número de teléfono. |
| Attribute-Id      | 0.9.2342.19200300.100.1.20                                                       |
| System-ID-GUID    | f0f8ffa1-1191-11d0-a060-00aa006c33ed                                             |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                      |



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
| Identificador de vínculo                | \-                                                                 |
| MAPI-Id                | 0x3A09                                                             |
| System-Only            | False                                                              |
| Tiene un único valor       | True                                                               |
| Está indexado             | False                                                              |
| En el catálogo global      | True                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Tiene un único valor       | True                                                                                                                                                     |
| Está indexado             | False                                                                                                                                                    |
| En el catálogo global      | True                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Tiene un único valor       | True                                                                                                                                                     |
| Está indexado             | False                                                                                                                                                    |
| En el catálogo global      | True                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Tiene un único valor       | True                                                                                                                                                     |
| Está indexado             | False                                                                                                                                                    |
| En el catálogo global      | True                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Tiene un único valor       | True                                                                                                                                                     |
| Está indexado             | False                                                                                                                                                    |
| En el catálogo global      | True                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Tiene un único valor       | True                                                                                                                                                     |
| Está indexado             | False                                                                                                                                                    |
| En el catálogo global      | True                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuario**](c-user.md)<br/> |



 

 





