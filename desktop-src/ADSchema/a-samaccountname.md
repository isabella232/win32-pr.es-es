---
title: Atributo SAM-Account-Name
description: Nombre de inicio de sesión usado para admitir clientes y servidores que ejecutan versiones anteriores del sistema operativo, como Windows NT 4.0, Windows 95, Windows 98 y LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo SAM-Account-Name
- Esquema de AD del atributo sAMAccountName
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74aa558f63c2e1822f1435cdafd6290755b92b4d5e34c329d8472693f37185d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022233"
---
# <a name="sam-account-name-attribute"></a>Atributo SAM-Account-Name

Nombre de inicio de sesión usado para admitir clientes y servidores que ejecutan versiones anteriores del sistema operativo, como Windows NT 4.0, Windows 95, Windows 98 y LAN Manager.

Este atributo debe tener 20 caracteres o menos para admitir clientes anteriores y no puede contener ninguno de estos caracteres:

-   "/ \\ \[ \] : ; \| = , + \* ? < >



| Entrada | Value |
|-------------------|------------------------------------------------------------------------------------------|
| CN                | SAM-Account-Name                                                                         |
| Ldap-Display-Name | sAMAccountName                                                                           |
| Size              | 20 caracteres o menos.                                                                   |
| Actualizar privilegios  | Administrador de dominio                                                                     |
| Frecuencia de actualización  | Este valor se debe asignar cuando se crea el registro de cuenta y no debe cambiar. |
| Attribute-Id      | 1.2.840.113556.1.4.221                                                                   |
| System-Id-Guid    | 3e0abfd0-126a-11d0-a060-00aa006c33ed                                                     |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                              |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



 

 





