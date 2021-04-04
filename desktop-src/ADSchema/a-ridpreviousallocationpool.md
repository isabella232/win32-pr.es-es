---
title: RID-Previous-Allocation-Pool (atributo)
description: Contiene el grupo de identificadores relativos (RID) del que un controlador de dominio asigna.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- RID-Previous-Allocation-Pool atributo AD Schema
- rIDPreviousAllocationPool esquema de AD de atributos
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905927"
---
# <a name="rid-previous-allocation-pool-attribute"></a>RID-Previous-Allocation-Pool (atributo)

El atributo **RID-Previous-Allocation-Pool** contiene el grupo de identificadores relativos (RID) del que un controlador de dominio asigna. Este atributo es un valor de ocho bytes que contiene un par de enteros de cuatro bytes que representan los valores inicial y final del grupo RID. El valor de inicio está en los cuatro bytes inferiores y el valor final está en los cuatro bytes superiores.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | RID-anterior: Grupo de asignación         |
| Nombre para mostrar de LDAP | rIDPreviousAllocationPool            |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.372               |
| System-ID-GUID    | 6617188a-8f3c-11d0-afda-00c04fd930c9 |
| Sintaxis            | [**Interval**](s-interval.md)       |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|----------------------------------------|
| Identificador de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | True                                   |
| Tiene un único valor       | True                                   |
| Está indexado             | False                                  |
| En el catálogo global      | False                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**RID: conjunto**](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------|
| Identificador de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | True                                   |
| Tiene un único valor       | True                                   |
| Está indexado             | False                                  |
| En el catálogo global      | False                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**RID: conjunto**](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------|
| Identificador de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | True                                   |
| Tiene un único valor       | True                                   |
| Está indexado             | False                                  |
| En el catálogo global      | False                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**RID: conjunto**](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------|
| Identificador de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | True                                   |
| Tiene un único valor       | True                                   |
| Está indexado             | False                                  |
| En el catálogo global      | False                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**RID: conjunto**](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------|
| Identificador de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | True                                   |
| Tiene un único valor       | True                                   |
| Está indexado             | False                                  |
| En el catálogo global      | False                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**RID: conjunto**](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------|
| Identificador de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | True                                   |
| Tiene un único valor       | True                                   |
| Está indexado             | False                                  |
| En el catálogo global      | False                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**RID: conjunto**](c-ridset.md)<br/> |



 

 





