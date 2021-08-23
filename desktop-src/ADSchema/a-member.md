---
title: Atributo de miembro
description: Lista de usuarios que pertenecen al grupo.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de miembro
- esquema de AD de atributo de miembro
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1efe13163946cb5be6ca83b5d0c7f964b8d6b1981ce45f79166af01bd62e6c9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705515"
---
# <a name="member-attribute"></a>Atributo de miembro

Lista de usuarios que pertenecen al grupo.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Miembro                                                |
| Ldap-Display-Name | miembro                                                |
| Size              | \-                                                    |
| Privilegio actualizar  | Administrador de dominio                                  |
| Frecuencia de actualización  | Cada vez que se agrega o quita un usuario de un grupo. |
| Attribute-Id      | 2.5.4.31                                              |
| System-Id-Guid    | bf9679c0-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)               |



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
|------------------------|-----------------------------------------------------------------------------------------|
| Id. de vínculo                | 2                                                                                       |
| MAPI-Id                | 0x8009                                                                                  |
| System-Only            | Falso                                                                                   |
| Es de un solo valor       | Falso                                                                                   |
| Está indexado             | Falso                                                                                   |
| En el catálogo global      | Verdadero                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000012                                                                              |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| Es de un solo valor       | Falso                                                                                                                                 |
| Está indexado             | Falso                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|-------------------------------------|
| Id. de vínculo                | 2                                   |
| MAPI-Id                | 0x8009                              |
| System-Only            | Falso                               |
| Es de un solo valor       | Falso                               |
| Está indexado             | Falso                               |
| En el catálogo global      | Verdadero                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000012                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| Es de un solo valor       | Falso                                                                                                                                 |
| Está indexado             | Falso                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| Es de un solo valor       | Falso                                                                                                                                 |
| Está indexado             | Falso                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| Es de un solo valor       | Falso                                                                                                                                 |
| Está indexado             | Falso                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| Es de un solo valor       | Falso                                                                                                                                 |
| Está indexado             | Falso                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> [**Grupo de nombres**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



 

 





