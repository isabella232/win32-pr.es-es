---
title: Atributo RID-Previous-Allocation-Pool
description: Contiene el grupo de identificadores relativos (RID) a los que un controlador de dominio asigna.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo RID-Previous-Allocation-Pool
- rIDPreviousAllocationPool attribute AD Schema
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5199d9fd0f91b94ed6625a8759f3a5acd76a892460c44e3315911350f0ff59f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837365"
---
# <a name="rid-previous-allocation-pool-attribute"></a>Atributo RID-Previous-Allocation-Pool

El **atributo RID-Previous-Allocation-Pool** contiene el grupo de identificadores relativos (RID) a los que asigna un controlador de dominio. Este atributo es un valor de ocho bytes que contiene un par de enteros de cuatro bytes que representan los valores inicial y final del grupo de RID. El valor inicial está en los cuatro bytes inferiores y el valor final está en los cuatro bytes superiores.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | RID-Previous-Allocation-Pool         |
| Ldap-Display-Name | rIDPreviousAllocationPool            |
| Size              | \-                                   |
| Actualizar privilegios  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.372               |
| System-Id-Guid    | 6617188a-8f3c-11d0-afda-00c04fd930c9 |
| Syntax            | [**Intervalo**](s-interval.md)       |



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
| Id. de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadero                                   |
| Es de un solo valor       | Verdadero                                   |
| Está indexado             | Falso                                  |
| En el catálogo global      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**Conjunto de RID**](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------|
| Id. de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadero                                   |
| Es de un solo valor       | Verdadero                                   |
| Está indexado             | Falso                                  |
| En el catálogo global      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**Conjunto de RID**](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------|
| Id. de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadero                                   |
| Es de un solo valor       | Verdadero                                   |
| Está indexado             | Falso                                  |
| En el catálogo global      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**Conjunto de RID**](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------|
| Id. de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadero                                   |
| Es de un solo valor       | Verdadero                                   |
| Está indexado             | Falso                                  |
| En el catálogo global      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**CONJUNTO DE RID**](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------|
| Id. de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadero                                   |
| Es de un solo valor       | Verdadero                                   |
| Está indexado             | Falso                                  |
| En el catálogo global      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**CONJUNTO DE RID**](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------|
| Id. de vínculo                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadero                                   |
| Es de un solo valor       | Verdadero                                   |
| Está indexado             | Falso                                  |
| En el catálogo global      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Clases usadas en        | [**CONJUNTO DE RID**](c-ridset.md)<br/> |



 

 





