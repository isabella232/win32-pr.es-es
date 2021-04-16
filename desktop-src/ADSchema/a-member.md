---
title: Atributo de miembro
description: La lista de usuarios que pertenecen al grupo.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Atributo de miembro esquema de AD
- atributo de miembro esquema de AD
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658598"
---
# <a name="member-attribute"></a>Atributo de miembro

La lista de usuarios que pertenecen al grupo.



| Entrada | Value |
|-------------------|-------------------------------------------------------|
| CN                | Miembro                                                |
| Nombre para mostrar de LDAP | miembro                                                |
| Tamaño              | \-                                                    |
| Actualizar privilegio  | Administrador de dominio                                  |
| Frecuencia de actualización  | Cada vez que se agrega o se quita un usuario de un grupo. |
| Attribute-Id      | 2.5.4.31                                              |
| System-ID-GUID    | bf9679c0-0de6-11d0-a285-00aa003049e2                  |
| Sintaxis            | [**Object(DS-DN)**](s-object-ds-dn.md)               |



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
|------------------------|-----------------------------------------------------------------------------------------|
| Identificador de vínculo                | 2                                                                                       |
| MAPI-Id                | 0x8009                                                                                  |
| System-Only            | False                                                                                   |
| Tiene un único valor       | False                                                                                   |
| Está indexado             | False                                                                                   |
| En el catálogo global      | True                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000012                                                                              |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Tiene un único valor       | False                                                                                                                                 |
| Está indexado             | False                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> [**MSMQ: Grupo**](c-msmq-group.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|-------------------------------------|
| Identificador de vínculo                | 2                                   |
| MAPI-Id                | 0x8009                              |
| System-Only            | False                               |
| Tiene un único valor       | False                               |
| Está indexado             | False                               |
| En el catálogo global      | True                                |
| Descriptor de NT-Security- | O:BAG: BAD: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000012                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Tiene un único valor       | False                                                                                                                                 |
| Está indexado             | False                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> [**MSMQ: Grupo**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Tiene un único valor       | False                                                                                                                                 |
| Está indexado             | False                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> [**MSMQ: Grupo**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Tiene un único valor       | False                                                                                                                                 |
| Está indexado             | False                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> [**MSMQ: Grupo**](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Tiene un único valor       | False                                                                                                                                 |
| Está indexado             | False                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> [**MSMQ: Grupo**](c-msmq-group.md)<br/> |



 

 





