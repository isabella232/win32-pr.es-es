---
title: Atributo User-Principal-Name
description: Este atributo contiene el UPN que es un nombre de inicio de sesión de estilo Internet para un usuario basado en el estándar de Internet RFC 822.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo User-Principal-Name
- UserPrincipalName attribute AD Schema (Esquema de AD del atributo userPrincipalName)
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba8ac5196de660c4cff4b90801470581cc660491902ec5b48f0ced8337c498b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835290"
---
# <a name="user-principal-name-attribute"></a>Atributo User-Principal-Name

Este atributo contiene el UPN que es un nombre de inicio de sesión de estilo Internet para un usuario basado en el estándar de Internet [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). El UPN es más corto que el nombre distintivo y es más fácil de recordar. Por convención, debe asignarse al nombre de correo electrónico del usuario. El valor establecido para este atributo es igual a la longitud del identificador del usuario y el nombre de dominio. Para obtener más información sobre este atributo, vea [Atributos de nomenclatura de usuario](/windows/desktop/AD/naming-properties).



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | User-Principal-Name                         |
| Ldap-Display-Name | userPrincipalName                           |
| Size              | \-                                          |
| Actualizar privilegios  | Administrador de dominio o propietario de la cuenta.      |
| Frecuencia de actualización  | En teoría, esto nunca debería cambiar.         |
| Attribute-Id      | 1.2.840.113556.1.4.656                      |
| System-Id-Guid    | 28630ebb-41d5-11d1-a9c1-0000f80367c1        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Verdadero                              |
| En el catálogo global      | Verdadero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Verdadero                              |
| En el catálogo global      | Verdadero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|--------------|
| Id. de vínculo                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Falso        |
| Es de un solo valor       | Verdadero         |
| Está indexado             | Verdadero         |
| En el catálogo global      | Verdadero         |
| NT-Security-Descriptor | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000001   |
| System-Flags           | 0x00000012   |
| Clases usadas en        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Verdadero                              |
| En el catálogo global      | Verdadero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Verdadero                              |
| En el catálogo global      | Verdadero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Verdadero                              |
| En el catálogo global      | Verdadero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Verdadero                              |
| En el catálogo global      | Verdadero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="remarks"></a>Comentarios

En ADAM, no es necesario que este atributo esté en el formato RFC 822 estándar de Internet; puede ser un nombre simple.

 

