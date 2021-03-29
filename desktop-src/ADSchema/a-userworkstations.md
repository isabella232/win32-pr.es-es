---
title: User-Workstations atributo)
description: Contiene los nombres NetBIOS o DNS de los equipos que ejecutan Windows NT Workstation o Windows 2000 Professional desde los que el usuario puede iniciar sesión.
ms.assetid: 92af070b-dadd-404d-8305-d85974639958
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de User-Workstations
- userWorkstations esquema de AD de atributos
topic_type:
- apiref
api_name:
- User-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cad59905dbf24c8baa13969d9a2ce5452767163
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905903"
---
# <a name="user-workstations-attribute"></a>User-Workstations atributo)

Contiene los nombres NetBIOS o DNS de los equipos que ejecutan Windows NT Workstation o Windows 2000 Professional desde los que el usuario puede iniciar sesión. Cada nombre NetBIOS está separado por una coma. Los nombres múltiples deben separarse con comas.

>[!Note]
>Este atributo de usuario ya no se debe usar. Para administrar qué cuentas pueden iniciar sesión en cada estación de trabajo, se recomienda usar "permitir el inicio de sesión local" y "denegar el inicio de sesión local" o "permitir el inicio de sesión a través de Servicios de Escritorio remoto" y "denegar el inicio de sesión a través de Servicios de Escritorio remoto".

| Entrada | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| CN                | User-Workstations                                                                          |
| Nombre para mostrar de LDAP | userWorkstations                                                                           |
| Tamaño              | \-                                                                                         |
| Actualizar privilegio  | Administrador de dominio o propietario de la cuenta.                                                     |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que es necesario cambiar el privilegio de inicio de sesión del usuario. |
| Attribute-Id      | 1.2.840.113556.1.4.86                                                                      |
| System-ID-GUID    | bf9679d7-0de6-11d0-a285-00aa003049e2                                                       |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                                |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



 

 





