---
title: Atributo de nombre principal de usuario
description: Este atributo contiene el UPN que es un nombre de inicio de sesión de estilo Internet para un usuario basado en el estándar de Internet RFC 822.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de nombre principal de usuario
- atributo userPrincipalName esquema de AD
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdb5bde76325409e0911615d1d21b1b4f593c06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997356"
---
# <a name="user-principal-name-attribute"></a>Atributo de nombre principal de usuario

Este atributo contiene el UPN que es un nombre de inicio de sesión de estilo Internet para un usuario basado en el estándar de Internet [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). El UPN es más corto que el nombre distintivo y más fácil de recordar. Por Convención, se debe asignar al nombre de correo electrónico del usuario. El valor establecido para este atributo es igual a la longitud del identificador del usuario y el nombre de dominio. Para obtener más información sobre este atributo, vea [atributos de asignación de nombres de usuario](/windows/desktop/AD/naming-properties).



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | User-Principal-Name                         |
| Nombre para mostrar de LDAP | userPrincipalName                           |
| Tamaño              | \-                                          |
| Actualizar privilegio  | Administrador de dominio o propietario de la cuenta.      |
| Frecuencia de actualización  | En teoría, esto nunca debería cambiar.         |
| Attribute-Id      | 1.2.840.113556.1.4.656                      |
| System-ID-GUID    | 28630ebb-41d5-11d1-a9c1-0000f80367c1        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|--------------|
| Identificador de vínculo                | \-           |
| MAPI-Id                | \-           |
| System-Only            | False        |
| Tiene un único valor       | True         |
| Está indexado             | True         |
| En el catálogo global      | True         |
| Descriptor de NT-Security- | O:BAG: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000001   |
| System-Flags           | 0x00000012   |
| Clases usadas en        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="remarks"></a>Observaciones

En ADAM, no es necesario que este atributo tenga el formato estándar de Internet RFC 822. puede ser un nombre simple.

 

