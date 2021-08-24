---
title: Atributo ms-DFSR-Schedule
description: Contiene la programación de replicación para el Sistema de archivos distribuido replicación de datos (DFS).
ms.assetid: 6dfcce16-44a4-4f7a-93ba-0c0d50605682
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DFSR-Schedule
- Esquema de AD del atributo msDFSR-Schedule
topic_type:
- apiref
api_name:
- ms-DFSR-Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7c2b9d151ddf369fb8d52ea98343f88a144019139d919d34b4b51247e2a121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119298215"
---
# <a name="ms-dfsr-schedule-attribute"></a>Atributo ms-DFSR-Schedule

Contiene la programación de replicación para el Sistema de archivos distribuido replicación de datos (DFS).



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | ms-DFSR-Schedule                                      |
| Ldap-Display-Name | msDFSR-Schedule                                       |
| Size              | \-                                                    |
| Actualizar privilegios  | \-                                                    |
| Frecuencia de actualización  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.6.13.3.14                            |
| System-Id-Guid    | 4699f15f-a71f-48e2-9ff5-5897c0759205                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | Falso                                                                                                                                 |
| Es de un solo valor       | True                                                                                                                                  |
| Está indexado             | Falso                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Clases usadas en        | [**ms-DFSR-ReplicationGroup**](c-msdfsr-replicationgroup.md)<br/> [**ms-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | Falso                                                                                                                                 |
| Es de un solo valor       | True                                                                                                                                  |
| Está indexado             | Falso                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Clases usadas en        | [**ms-DFSR-ReplicationGroup**](c-msdfsr-replicationgroup.md)<br/> [**ms-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | Falso                                                                                                                                 |
| Es de un solo valor       | Verdadero                                                                                                                                  |
| Está indexado             | Falso                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Clases usadas en        | [**ms-DFSR-ReplicationGroup**](c-msdfsr-replicationgroup.md)<br/> [**ms-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | Falso                                                                                                                                 |
| Es de un solo valor       | True                                                                                                                                  |
| Está indexado             | Falso                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Clases usadas en        | [**ms-DFSR-ReplicationGroup**](c-msdfsr-replicationgroup.md)<br/> [**ms-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="remarks"></a>Comentarios

El atributo forma parte de la compatibilidad del servicio de replicación Sistema de archivos distribuido (DFS).

 

 





