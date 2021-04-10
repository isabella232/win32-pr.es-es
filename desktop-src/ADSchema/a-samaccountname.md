---
title: Atributo SAM-Account-Name
description: Nombre de inicio de sesión que se usa para admitir clientes y servidores que ejecutan versiones anteriores del sistema operativo, como Windows NT 4,0, Windows 95, Windows 98 y LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de nombre de cuenta SAM
- atributo sAMAccountName esquema de AD
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906114"
---
# <a name="sam-account-name-attribute"></a>Atributo SAM-Account-Name

Nombre de inicio de sesión que se usa para admitir clientes y servidores que ejecutan versiones anteriores del sistema operativo, como Windows NT 4,0, Windows 95, Windows 98 y LAN Manager.

Este atributo debe tener 20 caracteres o menos para admitir clientes anteriores y no puede contener ninguno de estos caracteres:

-   "/ \\ \[ \] : ; \| = , + \* ? < >



| Entrada | Value |
|-------------------|------------------------------------------------------------------------------------------|
| CN                | Nombre de cuenta SAM                                                                         |
| Nombre para mostrar de LDAP | sAMAccountName                                                                           |
| Tamaño              | 20 caracteres o menos.                                                                   |
| Actualizar privilegio  | Administrador de dominio                                                                     |
| Frecuencia de actualización  | Este valor debe asignarse cuando se crea el registro de cuenta y no debe cambiar. |
| Attribute-Id      | 1.2.840.113556.1.4.221                                                                   |
| System-ID-GUID    | 3e0abfd0-126a-11d0-a060-00aa006c33ed                                                     |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                              |



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
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



 

 





