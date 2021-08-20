---
title: Admin-Count atributo
description: Indica que un objeto determinado ha cambiado sus ACL a un valor más seguro por el sistema porque era miembro de uno de los grupos administrativos (directa o transitivamente).
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Admin-Count esquema de AD de atributo
- AdminCount attribute AD Schema (Esquema de AD del atributo adminCount)
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d652d53627643e1028ee73cc67678119c689e46d8f4ec289c92ca32127e098dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022853"
---
# <a name="admin-count-attribute"></a>Admin-Count atributo

Indica que un objeto determinado ha cambiado sus ACL a un valor más seguro por el sistema porque era miembro de uno de los grupos administrativos (directa o transitivamente).



| Entrada | Value |
|-------------------|-----------------------------------------------------|
| CN                | Admin-Count                                         |
| Ldap-Display-Name | adminCount                                          |
| Size              | 4 bytes                                             |
| Actualizar privilegios  | El sistema establece este valor.                    |
| Frecuencia de actualización  | Cuando se agrega un objeto a un grupo administrativo. |
| Attribute-Id      | 1.2.840.113556.1.4.150                              |
| System-Id-Guid    | bf967918-0de6-11d0-a285-00aa003049e2                |
| Syntax            | [**Enumeración**](s-enumeration.md)                |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Es de un solo valor       | Verdadero                                                                  |
| Está indexado             | Falso                                                                 |
| En el catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Es de un solo valor       | Verdadero                                                                  |
| Está indexado             | Falso                                                                 |
| En el catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Es de un solo valor       | Verdadero                                                                  |
| Está indexado             | Falso                                                                 |
| En el catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Es de un solo valor       | Verdadero                                                                  |
| Está indexado             | Falso                                                                 |
| En el catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Es de un solo valor       | Verdadero                                                                  |
| Está indexado             | Falso                                                                 |
| En el catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Es de un solo valor       | Verdadero                                                                  |
| Está indexado             | Falso                                                                 |
| En el catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Usuario**](c-user.md)<br/> |



 

 





