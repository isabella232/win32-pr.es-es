---
title: Security-Identifier atributo)
description: Un valor único de longitud variable que se usa para identificar una cuenta de usuario, una cuenta de grupo o una sesión de inicio de sesión a la que se aplica una ACE.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Security-Identifier
- atributo securityIdentifier esquema de AD
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd921d0bcba08c2174475007476add8e8787456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804549"
---
# <a name="security-identifier-attribute"></a>Security-Identifier atributo)

Un valor único de longitud variable que se usa para identificar una cuenta de usuario, una cuenta de grupo o una sesión de inicio de sesión a la que se aplica una ACE.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Security-Identifier                  |
| Nombre para mostrar de LDAP | securityIdentifier                   |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.121               |
| System-ID-GUID    | bf967a2f-0de6-11d0-a285-00aa003049e2 |
| Sintaxis            | [**Cadena (SID)**](s-string-sid.md)  |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Tiene un único valor       | True                                                                                                              |
| Está indexado             | False                                                                                                             |
| En el catálogo global      | False                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Tiene un único valor       | True                                                                                                              |
| Está indexado             | False                                                                                                             |
| En el catálogo global      | True                                                                                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Tiene un único valor       | True                                                                                                              |
| Está indexado             | False                                                                                                             |
| En el catálogo global      | True                                                                                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Tiene un único valor       | True                                                                                                              |
| Está indexado             | False                                                                                                             |
| En el catálogo global      | True                                                                                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Tiene un único valor       | True                                                                                                              |
| Está indexado             | False                                                                                                             |
| En el catálogo global      | True                                                                                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Tiene un único valor       | True                                                                                                              |
| Está indexado             | False                                                                                                             |
| En el catálogo global      | True                                                                                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



 

 





